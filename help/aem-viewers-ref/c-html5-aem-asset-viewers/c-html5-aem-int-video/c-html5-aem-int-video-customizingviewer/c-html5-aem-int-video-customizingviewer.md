---
description: La personnalisation visuelle et la personnalisation comportementale la plus importante pour la visionneuse de vidéos interactive sont effectuées en créant une page CSS personnalisée.
keywords: réactif
solution: Experience Manager
title: Personnalisation de la visionneuse de vidéos interactive
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéos interactives
role: Développeur, Professionnel
exl-id: c428c3e6-81be-4708-b064-f9d794183209
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---

# Personnalisation de la visionneuse de vidéos interactives{#customizing-interactive-video-viewer}

La personnalisation visuelle et la personnalisation comportementale la plus importante pour la visionneuse de vidéos interactive sont effectuées en créant une page CSS personnalisée.

Le processus suggéré consiste à extraire le fichier CSS par défaut pour la visionneuse appropriée, à le copier vers un autre emplacement, à le personnaliser et à spécifier l’emplacement du fichier personnalisé dans la commande `style=`.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/InteractiveVideoViewer_dark.css`

Le lecteur est fourni avec deux fichiers CSS prêts à l’emploi, pour les modèles de couleurs &quot;clair&quot; et &quot;foncé&quot;. La version &quot;sombre&quot; est utilisée par défaut, mais il est facile de passer à la version &quot;légère&quot; en utilisant la page CSS standard suivante :

`<s7_viewers_root>/html5/InteractiveVideoViewer_light.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que celles par défaut. Si une déclaration de classe est omise, le lecteur ne fonctionne pas correctement car il ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre façon de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement sur la page Web ou dans l’une des règles CSS externes liées.

Lors de la création d’une page CSS personnalisée, gardez à l’esprit que le lecteur affecte une classe `.s7interactivevideoviewer` à son élément DOM conteneur. Si vous utilisez un fichier CSS externe transmis avec la commande `style=`, utilisez la classe `.s7interactivevideoviewer` en tant que classe parent dans le sélecteur descendant pour vos règles CSS. Si vous faites des styles incorporés sur la page Web, qualifiez en outre ce sélecteur avec l’identifiant de l’élément DOM du conteneur comme suit :

`#<containerId>.s7interactivevideoviewer`

## Création d&#39;une page CSS adaptée {#section-0bb49aca42d242d9b01879d5ba59d33b}

Il est possible de cible de différents périphériques et d’incorporer des tailles dans CSS pour que votre contenu s’affiche différemment selon le périphérique d’un utilisateur ou la mise en page d’une page Web particulière. Cela inclut, entre autres, les différentes mises en page, la taille des éléments de l’interface utilisateur et la résolution des illustrations.

Le lecteur prend en charge deux mécanismes de création d’une page CSS adaptée : Marqueurs CSS et requêtes multimédias CSS standard. Vous pouvez les utiliser séparément ou ensemble.

**Marqueurs CSS**

Pour faciliter la création de pages CSS adaptées, le lecteur prend en charge les marqueurs CSS. Il s’agit de classes CSS spéciales qui sont attribuées dynamiquement à l’élément de conteneur du lecteur de contenu de niveau supérieur en fonction de la taille du lecteur d’exécution et du type d’entrée utilisé sur le périphérique actuel.

Le premier groupe de marqueurs CSS comprend les classes `.s7size_large`, `.s7size_medium` et `.s7size_small`. Elles sont appliquées en fonction de la zone d’exécution du conteneur du lecteur de contenu. Si la zone de visualisation est égale ou supérieure à la taille d’un moniteur de bureau commun, `.s7size_large` est utilisé ; si la zone est proche d&#39;un périphérique tablette commun, `.s7size_medium` est affecté. Pour les zones similaires aux écrans de téléphone mobile, `.s7size_small` est défini. L’objectif Principal de ces marqueurs CSS est de créer différentes mises en page d’interface utilisateur pour différents écrans et tailles de visionneuse.

Le deuxième groupe de marqueurs CSS contient `.s7mouseinput` et `.s7touchinput`. `.s7touchinput` est défini si le périphérique actuel possède des capacités d&#39;entrée tactile ; sinon,  `.s7mouseinput` est utilisé. Ces marqueurs sont principalement destinés à créer des éléments d’entrée de l’interface utilisateur avec des tailles d’écran différentes pour différents types d’entrée, car en règle générale, la saisie tactile nécessite des éléments plus volumineux.

Le troisième groupe de marqueurs CSS contient `.s7device_landscape` et `.s7device_portrait`. `.s7device_landscape` est défini si le périphérique tactile est en orientation paysage ;  `.s7device_portrait` est utilisée lorsque l’utilisateur fait pivoter le périphérique tactile en orientation portrait. Ces marqueurs CSS sont destinés uniquement aux systèmes de bureau.

L’exemple de page CSS suivant définit la taille du bouton Lecture/Pause sur 28 x 28 pixels sur les systèmes avec entrée de la souris et 56 x 56 pixels sur les périphériques tactiles. En outre, il masque complètement le bouton si la taille de la visionneuse est réduite de manière significative :

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7interactivevideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7interactivevideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Dans l’exemple suivant, la barre de contrôle vidéo est positionnée à 138 pixels au-dessus du bas de la visionneuse si le périphérique tactile est en orientation portrait et déplacez-le tout en bas de la visionneuse dans tous les autres cas :

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7controlbar, 
.s7interactivevideoviewer.s7mouseinput .s7controlbar { 
 bottom:0px; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7controlbar { 
 bottom:136px; 
}
```

Pour cible des périphériques avec une densité de pixels différente, vous devez utiliser des requêtes de médias CSS. Le bloc de requête de média suivant contient des feuilles de style CSS spécifiques aux écrans haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation de marqueurs CSS est la méthode la plus souple de création de pages CSS adaptées, car elle vous permet de cible non seulement la taille de l’écran du périphérique, mais aussi la taille réelle de la visionneuse, ce qui est utile pour les mises en page adaptées.

Vous pouvez utiliser le fichier CSS de visionneuse par défaut comme exemple d’approche des marqueurs CSS.

**REQUÊTES de médias CSS**

Vous pouvez également exécuter la détection de périphérique en utilisant des requêtes multimédias CSS pures. Tout ce qui est inclus dans un bloc de requête de média donné est appliqué uniquement s&#39;il est exécuté sur un périphérique correspondant.

Lorsqu’elles sont appliquées aux visionneuses mobiles, elles utilisent quatre requêtes multimédias CSS, définies dans votre page CSS, dans l’ordre indiqué ci-dessous :

1. Contient uniquement des règles spécifiques à tous les périphériques tactiles.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. Contient uniquement des règles spécifiques aux tablettes avec écrans haute résolution.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Contient uniquement des règles spécifiques à tous les téléphones portables.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Contient uniquement des règles spécifiques aux téléphones portables dotés d’écrans haute résolution.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

En utilisant une approche de requêtes multimédia, vous devez organiser les pages CSS avec la détection de périphérique comme suit :

* Tout d’abord, la section spécifique à l’ordinateur de bureau définit toutes les propriétés spécifiques à l’ordinateur de bureau ou communes à tous les écrans.
* Ensuite, les quatre requêtes de médias suivent l’ordre défini ci-dessus et fournissent des règles CSS spécifiques au type de périphérique correspondant.

Il n’est pas nécessaire de duplicata de l’intégralité du fichier CSS du lecteur de contenu dans chaque requête multimédia. Seules les propriétés spécifiques à des périphériques donnés sont redéfinies dans une requête multimédia.

## CSS Sprites {#section-9b6d8d601cb441d08214dada7bb4eddc}

De nombreux éléments de l’interface utilisateur de la visionneuse sont mis en forme à l’aide d’illustrations bitmap et présentent plusieurs états visuels distincts. Un bon exemple est un bouton qui a normalement au moins 3 états différents : &quot;up&quot;, &quot;over&quot; et &quot;down&quot;. Chaque état requiert l’attribution de sa propre illustration bitmap.

Avec une approche classique de la mise en forme, le fichier CSS aurait une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de page CSS pour la mise en forme d’un bouton plein écran :

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

L’inconvénient de cette approche est que l’utilisateur final subit un scintillement ou une réponse différée de l’interface utilisateur lorsque l’élément est interagi pour la première fois. Cette action se produit car l’illustration de l’image pour le nouvel état d’élément n’est pas encore téléchargée. En outre, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

Les sprites CSS sont une approche différente selon laquelle les illustrations d’image pour tous les états d’élément sont combinées dans un fichier PNG unique appelé &quot;sprite&quot;. Un tel &quot;sprite&quot; a tous les états visuels pour l’élément donné positionné l’un après l’autre. Lors de la mise en forme d’un élément d’interface utilisateur avec des images-objets, la même image-objet est référencée pour tous les états différents du CSS. En outre, la propriété `background-position` est utilisée pour chaque état pour spécifier la partie de l’image &quot;sprite&quot; utilisée. Vous pouvez structurer une image &quot;sprite&quot; de n’importe quelle manière appropriée. Normalement, les visionneuses sont empilées verticalement. Vous trouverez ci-dessous un exemple de style basé sur des &quot;sprites&quot;, consistant à mettre en forme le même bouton plein écran précédemment :

```
.s7interactivevideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Notes et conseils généraux sur le style {#section-95855dccbbc444e79970f1aaa3260b7b}

* Lors de la personnalisation de l’interface utilisateur du lecteur avec CSS, l’utilisation de la règle `!IMPORTANT` n’est pas prise en charge pour mettre en forme les éléments de la visionneuse. En particulier, la règle `!IMPORTANT` ne doit pas être utilisée pour remplacer le style par défaut ou d’exécution fourni par le lecteur ou le SDK du lecteur de contenu. La raison en est qu&#39;elle peut affecter le comportement des composants appropriés. Vous devez plutôt utiliser des sélecteurs CSS avec la spécificité appropriée pour définir les propriétés CSS documentées dans ce guide de référence.

* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS, et non par rapport à l’emplacement de la page HTML de la visionneuse. Soyez conscient de cette règle lorsque vous copiez le fichier CSS par défaut vers un autre emplacement. Copiez également les ressources par défaut ou mettez à jour les chemins d’accès dans le fichier CSS personnalisé.
* Le format d’illustration bitmap préféré est le format PNG.
* L’illustration bitmap est affectée aux éléments de l’interface utilisateur à l’aide de la propriété `background-image`.
* Les propriétés `width` et `height` d&#39;un élément d&#39;interface utilisateur définissent sa taille logique. La taille du bitmap transmis à `background-image` n’affecte pas la taille logique.

* Pour utiliser la haute densité de pixels des écrans haute résolution comme Retina, spécifiez une illustration bitmap deux fois plus grande que la taille de l’élément d’interface utilisateur logique. Ensuite, appliquez la propriété `-webkit-background-size:contain` pour mettre à l’échelle l’arrière-plan en fonction de la taille de l’élément logique de l’interface utilisateur.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` à sa classe CSS.
* Vous pouvez utiliser divers formats pour la valeur de couleur prise en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

## Éléments communs de l&#39;interface utilisateur {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici la documentation de référence sur les éléments de l’interface utilisateur qui s’applique à la visionneuse de vidéos interactive :
