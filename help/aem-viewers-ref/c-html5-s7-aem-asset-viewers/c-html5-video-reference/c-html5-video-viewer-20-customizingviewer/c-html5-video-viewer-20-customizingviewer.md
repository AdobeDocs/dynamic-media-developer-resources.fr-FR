---
description: 'null'
keywords: responsive
seo-description: 'null'
seo-title: Personnalisation de la visionneuse vidéo
solution: Experience Manager
title: Personnalisation de la visionneuse vidéo
topic: Dynamic media
uuid: e18fdf8b-5834-4c99-b8a3-90d1f8310dc1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Personnalisation de la visionneuse vidéo{#customizing-video-viewer}

Toutes les personnalisations visuelles et la plupart des personnalisations de comportement sont effectuées en créant une page CSS personnalisée.

Le flux de travail suggéré consiste à extraire le fichier CSS par défaut pour la visionneuse appropriée, à le copier vers un autre emplacement, à le personnaliser et à spécifier l’emplacement du fichier personnalisé dans la `style=` commande.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/VideoViewer.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que les déclarations par défaut. Si une déclaration de classe est omise, le lecteur ne fonctionne pas correctement car il ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre manière de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement sur la page Web ou dans l’une des règles CSS externes liées.

Lorsque vous créez une page CSS personnalisée, n’oubliez pas que le lecteur affecte `.s7videoviewer` une classe à son élément DOM . Si vous utilisez un fichier CSS externe transmis avec la `style=` commande, utilisez `.s7videoviewer` class comme classe parent dans le sélecteur descendant pour vos règles CSS. Si vous incorporez des styles à la page Web, qualifiez en outre ce sélecteur avec un ID de l’élément DOM  comme suit :

`#<containerId>.s7videoviewer`

## Création de CSS adaptés {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

Il est possible d’de différents périphériques dans CSS pour que votre contenu s’affiche différemment selon le périphérique d’un utilisateur. Ce ciblage comprend, entre autres, différentes tailles d’éléments de l’interface utilisateur et différentes résolutions d’illustrations.

Le lecteur prend en charge deux mécanismes de création d’une page CSS adaptée : Marqueurs CSS et  de média CSS standard. Vous pouvez les utiliser indépendamment ou ensemble.

**Marqueurs CSS**

Pour faciliter la création d’une page CSS adaptée, le lecteur prend en charge les marqueurs CSS attribués dynamiquement aux classes CSS spéciales à l’élément de de la visionneuse de niveau supérieur en fonction de la taille de la visionneuse d’exécution et du type d’entrée utilisé sur le périphérique actuel.

Le premier groupe de marqueurs CSS comprend `.s7size_large`, `.s7size_medium`et `.s7size_small` des classes. Elles sont appliquées en fonction de la zone d’exécution du  du lecteur de contenu. En d’autres termes, si la zone du lecteur est égale ou supérieure à la taille d’un moniteur de bureau commun `.s7size_large` est utilisée; si la zone est proche de la taille d’une tablette commune `.s7size_medium` est affectée. Pour les zones similaires aux écrans de téléphone mobile `.s7size_small` est définie. L’objectif principal de ces marqueurs CSS est de créer différentes mises en page d’interface utilisateur pour différents écrans et tailles de visionneuse.

Le deuxième groupe de marqueurs CSS comprend `.s7mouseinput` et `.s7touchinput`. `.s7touchinput` est définie si le périphérique actif dispose de fonctionnalités d’entrée tactile ; dans le cas contraire, `.s7mouseinput` est utilisée. Ces marqueurs sont destinés à créer des éléments d’entrée de l’interface utilisateur avec des tailles d’écran différentes pour différents types d’entrée, car la saisie tactile requiert normalement des éléments plus volumineux. Si le périphérique dispose de fonctionnalités tactiles et d’entrée de souris, `.s7touchinput` est défini et le lecteur effectue le rendu d’une interface utilisateur tactile.

L’exemple de page CSS suivant définit la taille du bouton Lecture/Pause sur 28 x 28 pixels sur les systèmes avec entrée de souris et 56 x 56 pixels sur les périphériques tactiles. En outre, il masque complètement le bouton si la taille du lecteur devient vraiment petite :

```
.s7videoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7videoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7videoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Pour des périphériques avec une densité de pixels différente, utilisez le de médias CSS. Le bloc de multimédia suivant contiendra des feuilles CSS spécifiques aux écrans haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation des marqueurs CSS est la méthode la plus souple pour créer des feuilles CSS adaptées, car elle vous permet de non seulement la taille de l’écran du périphérique, mais aussi la taille réelle du lecteur, ce qui peut s’avérer utile pour les mises en page adaptées.

Utilisez le fichier CSS de la visionneuse par défaut comme exemple d’approche des marqueurs CSS.

**de médias CSS**

La détection de périphérique peut également être réalisée à l’aide de  de média CSS purs. Tout ce qui est contenu dans un bloc de de médias donné est appliqué uniquement lorsqu&#39;il est exécuté sur un périphérique correspondant.

Lorsqu’il est appliqué aux visionneuses mobiles, utilisez quatre  de de médias CSS, définis dans votre page CSS dans l’ordre indiqué ci-dessous :

1. Contient uniquement des règles spécifiques à tous les périphériques tactiles.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

À l’aide de l’approche de de médias CSS, vous devez organiser les feuilles de style CSS avec la détection de périphérique comme suit :

* Tout d’abord, la section spécifique au bureau définit toutes les propriétés qui sont spécifiques au bureau ou communes à tous les écrans.
* Ensuite, les quatre  de de médias doivent suivre l’ordre défini ci-dessus et fournir des règles CSS spécifiques au type de périphérique correspondant.

Il n’est pas nécessaire d’ l’intégralité du fichier CSS du lecteur dans chaque  de média. Seules les propriétés spécifiques à des périphériques donnés sont redéfinies dans un multimédia.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

De nombreux éléments de l’interface utilisateur du lecteur sont mis en forme à l’aide d’illustrations bitmap et présentent plusieurs états visuels distincts. Un bon exemple est un bouton qui a normalement 3 états différents : &quot;up&quot;, &quot;over&quot; et &quot;down&quot;. Chaque état requiert l’attribution de sa propre illustration bitmap.

Avec une approche classique de la mise en forme, le fichier CSS aurait une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de page CSS pour la mise en forme d’un bouton plein écran :

```
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

L’inconvénient de cette approche est que l’utilisateur final subit un scintillement ou une réponse différée de l’interface utilisateur lors de la première interaction de l’élément. Cette action se produit car l’illustration de l’image pour le nouvel état de l’élément n’est pas encore téléchargée. De plus, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

Les images-objets CSS sont une approche différente, où les illustrations d’image pour tous les états d’élément sont combinées dans un fichier PNG unique appelé &quot;image-objet&quot;. Un tel &quot;sprite&quot; a tous les états visuels pour l’élément donné positionné l’un après l’autre. Lors de la mise en forme d’un élément d’interface utilisateur avec des images-objets, la même image-objet est référencée pour tous les états différents du CSS. En outre, la `background-position` propriété est utilisée pour chaque état pour spécifier la partie de l’image &quot;sprite&quot; utilisée. Vous pouvez structurer une image &quot;sprite&quot; de n’importe quelle manière appropriée. Les lecteurs disposent normalement d’un empilement vertical. Vous trouverez ci-dessous un exemple de style basé sur des &quot;images-objets&quot; du même bouton plein écran depuis le dessus :

```
.s7videoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Notes et conseils de mise en forme générale {#section-097418bd618740bba36352629e4d88e1}

* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS et non par rapport à l’emplacement de la page HTML de la visionneuse. N’oubliez pas de tenir compte de cette règle lorsque vous copiez le fichier CSS par défaut à un autre emplacement. Copiez les fichiers par défaut ou mettez à jour les chemins d’accès dans le fichier CSS personnalisé.
* Le format préféré pour les illustrations bitmap est le format PNG.
* Les illustrations bitmap sont affectées aux éléments de l’interface utilisateur à l’aide de la `background-image` propriété.
* Les propriétés `width` et `height` les propriétés d’un élément d’interface utilisateur définissent sa taille logique. La taille du bitmap transmis à `background-image` n’affecte pas la taille logique.

* Pour utiliser la haute densité de pixels des écrans haute résolution comme Retina, spécifiez une illustration bitmap deux fois plus grande que la taille d’élément logique de l’interface utilisateur. Ensuite, appliquez la `-webkit-background-size:contain` propriété pour réduire l’arrière-plan à la taille de l’élément logique de l’interface utilisateur.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` à sa classe CSS.
* Vous pouvez utiliser divers formats pour la valeur de couleur prise en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

* Lors de la personnalisation de l’interface utilisateur du lecteur avec CSS, l’utilisation de la `!IMPORTANT` règle n’est pas prise en charge pour mettre en forme les éléments du lecteur. En particulier, `!IMPORTANT` la règle ne doit pas être utilisée pour remplacer le style par défaut ou d’exécution fourni par le lecteur ou le kit de développement de visionneuse. La raison en est qu&#39;elle peut affecter le comportement des composants appropriés. Utilisez plutôt des sélecteurs CSS avec la spécificité appropriée pour définir les propriétés CSS documentées dans ce guide de référence.

## Éléments communs de l’interface utilisateur {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici la documentation de référence sur les éléments de l’interface utilisateur qui s’applique à la visionneuse vidéo :
