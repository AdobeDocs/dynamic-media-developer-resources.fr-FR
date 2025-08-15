---
title: Personnalisation de la visionneuse de vidéos
description: Personnalisation de la visionneuse de vidéos
keywords: réactif
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 90dc93ee-fdd0-41c9-9eef-4c9952198356
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1265'
ht-degree: 0%

---

# Personnalisation de la visionneuse de vidéos{#customizing-video-viewer}

Toutes les personnalisations visuelles et la plupart des personnalisations comportementales sont effectuées en créant un CSS personnalisé.

Le processus suggéré consiste à prendre le fichier CSS par défaut pour la visionneuse appropriée, à le copier à un autre emplacement, à le personnaliser et à spécifier l’emplacement du fichier personnalisé dans la commande `style=`.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/VideoViewer.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que le fichier par défaut. Si une déclaration de classe est omise, la visionneuse ne fonctionne pas correctement, car elle ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre manière de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement dans la page web ou dans l’une des règles CSS externes liées.

Lorsque vous créez un CSS personnalisé, n’oubliez pas que la visionneuse attribue `.s7videoviewer` classe à son élément DOM conteneur. Si vous utilisez un fichier CSS externe transmis avec la commande `style=`, utilisez `.s7videoviewer` classe comme classe parente dans le sélecteur descendant pour vos règles CSS. Si vous incorporez des styles à la page web, qualifiez également ce sélecteur avec un identifiant de l’élément DOM du conteneur comme suit :

`#<containerId>.s7videoviewer`

## Création d’un CSS en responsive design {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

Il est possible de cibler différents appareils dans CSS pour que votre contenu s’affiche différemment selon l’appareil d’un utilisateur. Ce ciblage inclut, sans s’y limiter, différentes tailles d’élément de l’interface utilisateur et résolutions d’illustration.

La visionneuse prend en charge deux mécanismes de création de CSS conçus en responsive design : les marqueurs CSS et les requêtes multimédias CSS standard. Vous pouvez utiliser ces deux mécanismes indépendamment ou ensemble.

**Marqueurs CSS**

Pour vous aider à créer une feuille de style CSS en responsive design, la visionneuse prend en charge les marqueurs CSS qui des classes CSS spéciales sont affectées dynamiquement à l’élément de conteneur de visionneuse de niveau supérieur. L’affectation est basée sur la taille de la visionneuse au moment de l’exécution et le type d’entrée utilisé sur l’appareil actuel.

Le premier groupe de marqueurs CSS comprend les classes `.s7size_large`, `.s7size_medium` et `.s7size_small`. Elles sont appliquées en fonction de la zone d’exécution du conteneur de la visionneuse. En d’autres termes, si la zone de la visionneuse est égale ou supérieure à la taille d’un moniteur de bureau commun `.s7size_large` est utilisé, et si la zone est proche de la taille d’une tablette commune, `.s7size_medium` est attribué. Pour les zones similaires aux écrans de téléphone mobile, `.s7size_small` est défini. L’objectif principal de ces marqueurs CSS est de créer différentes dispositions d’interface utilisateur pour différents écrans et tailles de visionneuse.

Le deuxième groupe de marqueurs CSS comprend `.s7mouseinput` et `.s7touchinput`. Le marqueur `.s7touchinput` est défini si l’appareil actuel dispose de fonctionnalités d’entrée tactile ; dans le cas contraire, `.s7mouseinput` est utilisé. Ces marqueurs sont destinés à créer des éléments d’entrée de l’interface utilisateur avec différentes tailles d’écran pour différents types d’entrée, car normalement l’entrée tactile nécessite des éléments plus grands. Si l’appareil dispose à la fois des fonctionnalités d’entrée de souris et tactiles, `.s7touchinput` est défini et la visionneuse offre une interface utilisateur conviviale pour les écrans tactiles.

L’exemple de CSS suivant définit la taille du bouton de lecture/pause sur 28 x 28 pixels sur les systèmes dotés d’une entrée de souris et 56 x 56 pixels sur les appareils tactiles. En outre, il masque complètement le bouton si la taille de la visionneuse devient trop petite :

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

Pour cibler des appareils avec une densité de pixels différente, utilisez des requêtes multimédias CSS. Le bloc de requête de média suivant contient un CSS spécifique aux écrans haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation de marqueurs CSS est le moyen le plus flexible de créer un CSS réactif conçu. En effet, il vous permet de cibler non seulement la taille de l’écran de l’appareil, mais également la taille réelle de la visionneuse, ce qui peut s’avérer utile pour les mises en page des pages en Responsive Design.

Utilisez le fichier CSS de la visionneuse par défaut comme exemple d’approche de marqueurs CSS.

**Requêtes multimédias CSS**

La détection d’appareil peut également être effectuée à l’aide de requêtes multimédias CSS pures. Tous les éléments inclus dans un bloc de requête de média donné sont appliqués uniquement lorsqu’ils sont exécutés sur un appareil correspondant.

Lorsqu’elles sont appliquées aux visionneuses mobiles, utilisez quatre requêtes de média CSS, définies dans votre CSS dans l’ordre indiqué ci-dessous :

1. Contient uniquement des règles spécifiques à tous les appareils tactiles.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

1. Contient uniquement des règles spécifiques à tous les téléphones mobiles.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Contient uniquement des règles spécifiques aux téléphones mobiles dotés d’écrans haute résolution.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

En utilisant l’approche de requêtes multimédias CSS, vous devez organiser le CSS avec la détection d’appareil comme suit :

* Tout d’abord, la section spécifique au bureau définit toutes les propriétés qui sont spécifiques au bureau ou communes à tous les écrans.
* Deuxièmement, les quatre requêtes de média doivent s’exécuter dans l’ordre défini ci-dessus et fournir des règles CSS spécifiques au type d’appareil correspondant.

Il n’est pas nécessaire de dupliquer l’intégralité du CSS de la visionneuse dans chaque requête de média. Seules les propriétés spécifiques à des appareils donnés sont redéfinies dans une requête de média.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

De nombreux éléments de l’interface utilisateur de la visionneuse sont stylisés à l’aide d’illustrations bitmap et présentent plusieurs états visuels distincts. Un bon exemple est un bouton qui possède normalement au moins trois états différents : « up », « over » (supérieur), et « down » (inférieur). Chaque état nécessite l’attribution de sa propre illustration bitmap.

Avec une approche classique du style, le CSS dispose d’une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de CSS pour le style d’un bouton plein écran :

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

L’inconvénient de cette approche est que l’utilisateur final fait face à un scintillement ou à un retard de réponse de l’interface utilisateur lors de la première interaction avec l’élément. Cette action se produit, car l’illustration de l’image du nouvel état de l’élément n’a pas encore été téléchargée. En outre, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

CSS sprites est une approche différente où l’illustration d’image pour tous les états d’élément est combinée dans un seul fichier PNG appelé « sprite ». Ce « sprite » possède tous les états visuels pour l&#39;élément donné positionnés les uns à la suite des autres. Lors de la mise en forme d’un élément de l’interface utilisateur avec des sprites, la même image sprite est référencée pour tous les différents états dans le CSS. En outre, la propriété `background-position` est utilisée pour chaque état afin de spécifier quelle partie de l’image « sprite » est utilisée. Vous pouvez structurer une image « sprite » de n’importe quelle manière appropriée. Les visionneuses l’ont normalement empilé verticalement. Vous trouverez ci-dessous un exemple basé sur « sprite » de mise en forme du même bouton plein écran ci-dessus :

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

## Notes et conseils généraux sur le style {#section-097418bd618740bba36352629e4d88e1}

* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS et non par rapport à l’emplacement de la page HTML de la visionneuse. N’oubliez pas de tenir compte de cette règle lorsque vous copiez le fichier CSS par défaut vers un autre emplacement. Copiez les ressources par défaut ou mettez à jour les chemins d’accès dans le CSS personnalisé.
* Le format préféré pour les illustrations bitmap est PNG.
* L’illustration bitmap est affectée aux éléments de l’interface utilisateur à l’aide de la propriété `background-image`.
* Les propriétés `width` et `height` d’un élément de l’interface utilisateur définissent sa taille logique. La taille de l’image bitmap transmise à `background-image` n’affecte pas la taille logique.

* Pour utiliser la densité élevée en pixels des écrans haute résolution tels que Retina, spécifiez une illustration bitmap deux fois plus grande que la taille de l’élément de l’interface utilisateur logique. Appliquez ensuite la propriété `-webkit-background-size:contain` pour réduire l’arrière-plan à la taille de l’élément logique de l’interface utilisateur.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` à sa classe CSS.
* Vous pouvez utiliser différents formats pour les valeurs de couleur prises en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

* Lors de la personnalisation de l’interface utilisateur de la visionneuse avec CSS, l’utilisation de la règle `!IMPORTANT` n’est pas prise en charge pour appliquer un style aux éléments de la visionneuse. En particulier, `!IMPORTANT` règle ne doit pas être utilisée pour remplacer un style par défaut ou au moment de l’exécution fourni par la visionneuse ou le SDK de la visionneuse. En effet, cela peut affecter le comportement des composants appropriés. À la place, vous devez utiliser des sélecteurs CSS avec la spécificité appropriée pour définir les propriétés CSS qui sont documentées dans ce guide de référence.

## Éléments courants de l’interface utilisateur {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici la documentation de référence sur les éléments de l’interface utilisateur qui s’applique à la visionneuse de vidéos :
