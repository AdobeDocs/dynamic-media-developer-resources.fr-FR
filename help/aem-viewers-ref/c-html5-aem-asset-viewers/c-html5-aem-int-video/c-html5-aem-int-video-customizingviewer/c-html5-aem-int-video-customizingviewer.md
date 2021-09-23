---
title: Personnalisation de la visionneuse de vidéo interactive
description: Toutes les personnalisations visuelles et la plupart des personnalisations de comportement pour la visionneuse de vidéos interactives sont effectuées par la création d’une page CSS personnalisée.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c428c3e6-81be-4708-b064-f9d794183209
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 0%

---

# Personnalisation de la visionneuse de vidéo interactive{#customizing-interactive-video-viewer}

Toutes les personnalisations visuelles et la plupart des personnalisations de comportement pour la visionneuse de vidéos interactives sont effectuées par la création d’une page CSS personnalisée.

Le workflow suggéré consiste à prendre le fichier CSS par défaut pour la visionneuse appropriée, à le copier vers un autre emplacement, à le personnaliser, et à spécifier l’emplacement du fichier personnalisé dans la commande `style=`.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/InteractiveVideoViewer_dark.css`

La visionneuse est fournie avec deux fichiers CSS prêts à l’emploi, pour les schémas de couleurs &quot;clair&quot; et &quot;sombre&quot;. La version &quot;sombre&quot; est utilisée par défaut, mais il est facile de passer à la version &quot;légère&quot; à l’aide du CSS standard suivant :

`<s7_viewers_root>/html5/InteractiveVideoViewer_light.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que celles par défaut. Si une déclaration de classe est omise, la visionneuse ne fonctionne pas correctement, car elle ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre manière de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement sur la page web ou dans l’une des règles CSS externes liées.

Lors de la création d’une page CSS personnalisée, gardez à l’esprit que la visionneuse affecte la classe `.s7interactivevideoviewer` à son élément DOM de conteneur. Si vous utilisez un fichier CSS externe transmis avec la commande `style=`, utilisez la classe `.s7interactivevideoviewer` en tant que classe parente dans le sélecteur descendant pour vos règles CSS. Si vous effectuez des styles intégrés sur la page web, qualifiez ce sélecteur avec un identifiant de l’élément DOM du conteneur comme suit :

`#<containerId>.s7interactivevideoviewer`

## Création d’une page CSS adaptée {#section-0bb49aca42d242d9b01879d5ba59d33b}

Il est possible de cibler différents appareils et d’incorporer des tailles différentes dans une page CSS afin de faire afficher votre contenu différemment selon le périphérique ou la mise en page d’un utilisateur. Cette méthode comprend, sans s’y limiter, différentes mises en page, tailles d’éléments de l’interface utilisateur et résolution des illustrations.

La visionneuse prend en charge deux mécanismes de création d’une page CSS réactive : Marqueurs CSS et requêtes multimédias CSS standard. Vous pouvez utiliser ces mécanismes indépendamment ou ensemble.

**Marqueurs CSS**

Pour faciliter la création de CSS responsive design, la visionneuse prend en charge les marqueurs CSS. Ces marqueurs sont des classes CSS spéciales. Ils sont dynamiquement affectés à l’élément conteneur de la visionneuse de niveau supérieur en fonction de la taille de la visionneuse au moment de l’exécution et du type d’entrée utilisé sur l’appareil actuel.

Le premier groupe de marqueurs CSS comprend les classes `.s7size_large`, `.s7size_medium` et `.s7size_small`. Elles sont appliquées en fonction de la zone d’exécution du conteneur de la visionneuse. Si la zone de visionneuse est égale ou supérieure à la taille d’un écran de bureau commun, `.s7size_large` est utilisé. si la zone est proche d’une tablette commune, `.s7size_medium` est affecté. Pour les zones similaires aux écrans de téléphone mobile, `.s7size_small` est défini. L’objectif Principal de ces marqueurs CSS est de créer différentes mises en page d’interface utilisateur pour différents écrans et tailles de visionneuse.

Le deuxième groupe de marqueurs CSS contient `.s7mouseinput` et `.s7touchinput`. Le marqueur `.s7touchinput` est défini si l’appareil actuel dispose de fonctionnalités d’entrée tactile ; sinon, `.s7mouseinput` est utilisé. Ces marqueurs sont principalement destinés à créer des éléments d’entrée de l’interface utilisateur avec des tailles d’écran différentes pour différents types d’entrée, car la saisie tactile nécessite normalement des éléments plus volumineux.

Le troisième groupe de marqueurs CSS contient `.s7device_landscape` et `.s7device_portrait`. Le marqueur `.s7device_landscape` est défini si l’appareil tactile est en orientation paysage ; `.s7device_portrait` est utilisé lorsque l’appareil tactile est pivoté vers l’orientation portrait. Ces marqueurs CSS sont destinés uniquement aux systèmes de bureau.

L’exemple de page CSS suivant définit la taille du bouton de lecture/pause sur 28x28 pixels sur les systèmes avec une entrée de souris et 56x56 pixels sur les appareils tactiles. En outre, le bouton est entièrement masqué si la taille de la visionneuse est réduite de manière significative :

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

Dans l’exemple suivant, la barre de contrôle vidéo est positionnée à 138 pixels au-dessus du bas de la visionneuse si l’appareil tactile est en orientation portrait. Il est déplacé au bas de la visionneuse dans tous les autres cas :

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7controlbar, 
.s7interactivevideoviewer.s7mouseinput .s7controlbar { 
 bottom:0px; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7controlbar { 
 bottom:136px; 
}
```

Pour cibler des appareils avec une densité de pixels différente, vous devez utiliser des requêtes multimédias CSS. Le bloc de requête multimédia suivant contiendrait une feuille CSS spécifique aux écrans à haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation de marqueurs CSS est la méthode la plus souple pour créer des CSS responsive design, car elle vous permet de cibler non seulement la taille de l’écran de l’appareil, mais aussi la taille réelle de la visionneuse, ce qui est utile pour les mises en page Responsive Design.

Vous pouvez utiliser le fichier CSS de visionneuse par défaut comme exemple d’approche des marqueurs CSS.

**Requêtes de média CSS**

Vous pouvez également réaliser la détection de périphérique en utilisant des requêtes multimédias CSS pures. Tout ce qui est inclus dans un bloc de requête multimédia donné est appliqué uniquement lorsqu’il est exécuté sur un appareil correspondant.

Lorsqu’elles sont appliquées aux visionneuses mobiles, elles utilisent quatre requêtes multimédias CSS, définies dans votre CSS, dans l’ordre indiqué ci-dessous :

1. Contient uniquement des règles spécifiques à tous les appareils tactiles.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. Contient uniquement des règles spécifiques aux tablettes avec des écrans haute résolution.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Contient uniquement des règles spécifiques à tous les téléphones mobiles.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Contient uniquement des règles spécifiques aux téléphones mobiles avec écrans haute résolution.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

À l’aide d’une approche de requêtes de média, vous devez organiser CSS avec la détection de périphérique comme suit :

* Tout d’abord, la section spécifique à l’ordinateur de bureau définit toutes les propriétés spécifiques à l’ordinateur ou communes à tous les écrans.
* Deuxièmement, les quatre requêtes de média suivent l’ordre défini ci-dessus et fournissent des règles CSS spécifiques au type d’appareil correspondant.

Il n’est pas nécessaire de dupliquer l’intégralité du CSS de la visionneuse dans chaque requête de média. Seules les propriétés spécifiques à des appareils donnés sont redéfinies au sein d’une requête multimédia.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

De nombreux éléments de l’interface utilisateur de la visionneuse sont stylisés à l’aide d’illustrations bitmap et possèdent plusieurs états visuels distincts. Un bon exemple est un bouton qui comporte normalement au moins trois états différents : &quot;vers le haut&quot;, &quot;vers le bas&quot; et &quot;vers le bas&quot;. Chaque état nécessite l’attribution de sa propre illustration bitmap.

Avec une approche classique de la mise en forme, le CSS dispose d’une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de page CSS pour le style d’un bouton plein écran :

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

L’inconvénient de cette approche est que l’utilisateur final subit un scintillement ou une réponse de l’interface utilisateur différée lorsque l’élément est interagi pour la première fois. Cette action se produit car l’illustration de l’image pour le nouvel état d’élément n’est pas encore téléchargée. En outre, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

Les sprites CSS constituent une approche différente selon laquelle l’illustration d’image pour tous les états d’élément est combinée dans un seul fichier PNG appelé &quot;sprite&quot;. Un tel &quot;sprite&quot; a tous les états visuels pour l’élément donné positionnés l’un après l’autre. Lors du style d’un élément d’interface utilisateur avec des sprites, la même image de sprite est référencée pour tous les états différents du CSS. En outre, la propriété `background-position` est utilisée pour chaque état pour spécifier la partie de l’image &quot;sprite&quot; utilisée. Vous pouvez structurer une image &quot;sprite&quot; de n’importe quelle manière appropriée. Les visionneuses sont normalement empilées verticalement. Vous trouverez ci-dessous un exemple de style &quot;sprite&quot; du même bouton plein écran précédemment :

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

* Lors de la personnalisation de l’interface utilisateur de la visionneuse avec CSS, l’utilisation de la règle `!IMPORTANT` n’est pas prise en charge pour appliquer un style aux éléments de la visionneuse. En particulier, la règle `!IMPORTANT` ne doit pas être utilisée pour remplacer les styles par défaut ou d’exécution fournis par la visionneuse ou le SDK de la visionneuse. La raison est qu’elle peut affecter le comportement des composants appropriés. Vous devez plutôt utiliser des sélecteurs CSS avec la précision appropriée pour définir les propriétés CSS documentées dans ce guide de référence.

* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS, et non par rapport à l’emplacement de la page HTML de la visionneuse. Tenez compte de cette règle lorsque vous copiez le CSS par défaut vers un autre emplacement. Copiez également les ressources par défaut ou mettez à jour les chemins d’accès dans le fichier CSS personnalisé.
* Le format préféré des illustrations bitmap est PNG.
* Les illustrations bitmap sont affectées aux éléments de l’interface utilisateur à l’aide de la propriété `background-image` .
* Les propriétés `width` et `height` d’un élément d’interface utilisateur définissent sa taille logique. La taille de l’image bitmap transmise à `background-image` n’affecte pas la taille logique.

* Pour utiliser la haute densité en pixels d’écrans haute résolution comme Retina, spécifiez une illustration bitmap deux fois plus grande que la taille de l’élément logique de l’interface utilisateur. Ensuite, appliquez la propriété `-webkit-background-size:contain` pour mettre l’arrière-plan à l’échelle de la taille de l’élément logique de l’interface utilisateur.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` à sa classe CSS.
* Vous pouvez utiliser différents formats pour la valeur de couleur prise en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

## Éléments de l’interface utilisateur courants {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici une documentation de référence sur les éléments de l’interface utilisateur qui s’applique à la visionneuse de vidéo interactive :
