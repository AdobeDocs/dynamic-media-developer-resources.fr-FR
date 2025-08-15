---
title: Personnalisation de la visionneuse Zoom de base
description: Toutes les personnalisations visuelles et la plupart des personnalisations comportementales de la visionneuse Zoom de base sont effectuées en créant un CSS personnalisé.
keywords: réactif
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9cbce980-83fd-40a7-8bcd-f9bc4dd477a8
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '1339'
ht-degree: 0%

---

# Personnalisation de la visionneuse Zoom de base{#customizing-basic-zoom-viewer}

Toutes les personnalisations visuelles et la plupart des personnalisations comportementales de la visionneuse Zoom de base sont effectuées en créant un CSS personnalisé.

Le processus suggéré consiste à prendre le fichier CSS par défaut pour la visionneuse appropriée, à le copier à un autre emplacement, à le personnaliser et à spécifier l’emplacement du fichier personnalisé dans la commande `style=`.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/BasicZoomViewer_light.css`

La visionneuse est fournie avec deux fichiers CSS prêts à l’emploi, pour les modèles de couleurs « clair » et « sombre ». La version « light » est utilisée par défaut, mais vous pouvez passer à la version « dark » en utilisant le CSS standard suivant :

`<s7_viewers_root>/html5/BasicZoomViewer_dark.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que le fichier par défaut. Si une déclaration de classe est omise, la visionneuse ne fonctionne pas correctement, car elle ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre manière de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement dans la page web ou dans l’une des règles CSS externes liées.

Lors de la création d’un CSS personnalisé, gardez à l’esprit que la visionneuse attribue `.s7basiczoomviewer` classe à son élément DOM conteneur. Si vous utilisez un fichier CSS externe transmis avec `style=` commande, utilisez `.s7basiczoomviewer` classe comme classe parente dans le sélecteur descendant pour vos règles CSS. Si vous effectuez des styles incorporés sur la page web, qualifiez également ce sélecteur avec un identifiant de l’élément DOM du conteneur comme suit :

`#<containerId>.s7basiczoomviewer`

## Création d’un CSS de conception réactive {#section-0bb49aca42d242d9b01879d5ba59d33b}

Il est possible de cibler différents appareils et tailles d’incorporation dans le CSS pour faire en sorte que votre contenu s’affiche différemment selon l’appareil d’un utilisateur ou d’une utilisatrice ou une mise en page web particulière. Ce ciblage inclut, sans s’y limiter, différentes mises en page, tailles d’élément de l’interface utilisateur et résolution de l’illustration.

La visionneuse prend en charge deux mécanismes de création de CSS conçus en responsive design : les marqueurs CSS et les requêtes multimédias CSS standard. Vous pouvez utiliser ces mécanismes indépendamment ou ensemble.

**Marqueurs CSS**

Pour faciliter la création de CSS en responsive design, la visionneuse prend en charge les marqueurs CSS. Ces marqueurs sont des classes CSS spéciales. Ils sont affectés dynamiquement à l’élément de conteneur de visionneuse de niveau supérieur en fonction de la taille de la visionneuse au moment de l’exécution et du type d’entrée utilisé sur l’appareil actuel.

Le premier groupe de marqueurs CSS comprend les classes `.s7size_large`, `.s7size_medium` et `.s7size_small`. Elles sont appliquées en fonction de la zone d’exécution du conteneur de la visionneuse. Si la zone de la visionneuse est égale ou supérieure à la taille d’un moniteur de bureau commun, la `.s7size_large` est utilisée ; si la zone est proche d’une tablette commune, la `.s7size_medium` est attribuée. Pour les zones similaires aux écrans de téléphone mobile, `.s7size_small` est défini. L’objectif principal de ces marqueurs CSS est de créer différentes dispositions d’interface utilisateur pour différents écrans et tailles de visionneuse.

Le deuxième groupe de marqueurs CSS contient `.s7mouseinput` et `.s7touchinput`. Le marqueur de `.s7touchinput` est défini si l’appareil actuel dispose de fonctionnalités d’entrée tactile ; dans le cas contraire, `.s7mouseinput` est utilisé. Ces marqueurs sont principalement destinés à créer des éléments d’entrée de l’interface utilisateur avec différentes tailles d’écran pour différents types d’entrée, car l’entrée tactile nécessite normalement des éléments plus grands. Dans les cas où l’appareil dispose à la fois de fonctionnalités d’entrée de souris et tactiles, `.s7touchinput` est défini et la visionneuse offre une interface utilisateur conviviale pour les écrans tactiles.

L’exemple de CSS suivant définit la taille du bouton de zoom avant sur 28 x 28 pixels sur les systèmes dotés d’une entrée de souris et sur 56 x 56 pixels sur les appareils tactiles. En outre, le bouton est complètement masqué si la taille de la visionneuse devient réduite :

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7basiczoomviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7basiczoomviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Pour cibler des appareils avec une densité de pixels différente, vous devez utiliser des requêtes multimédias CSS. Le bloc de requête de média suivant contiendrait un CSS spécifique aux écrans haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation de marqueurs CSS est le moyen le plus flexible de créer du CSS pour le responsive design. En effet, il vous permet de cibler non seulement la taille de l’écran de l’appareil, mais aussi la taille réelle de la visionneuse, ce qui s’avère utile pour les mises en page en responsive design.

Vous pouvez utiliser le fichier CSS de visionneuse par défaut comme exemple d’approche de marques CSS.

**Requêtes multimédias CSS**

Vous pouvez également réaliser la détection d’appareil à l’aide de requêtes multimédias CSS pures. Tous les éléments inclus dans un bloc de requête de média donné sont appliqués uniquement lorsqu’ils sont exécutés sur un appareil correspondant.

Lorsqu’elles sont appliquées aux visionneuses mobiles, les quatre requêtes de média CSS, définies dans votre CSS, dans l’ordre indiqué ci-dessous :

1. Contient uniquement des règles spécifiques à tous les appareils tactiles.

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

En utilisant une approche de requêtes de média, vous devez organiser le CSS avec la détection d’appareil comme suit :

* Tout d’abord, la section spécifique au poste de travail définit toutes les propriétés qui sont spécifiques au poste de travail ou communes à tous les écrans.
* Ensuite, les quatre requêtes de média s’exécutent dans l’ordre défini ci-dessus et fournissent des règles CSS spécifiques au type d’appareil correspondant.

Il n’est pas nécessaire de dupliquer l’intégralité du CSS de la visionneuse dans chaque requête de média. Seules les propriétés spécifiques à des appareils donnés sont redéfinies dans une requête de média.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

De nombreux éléments de l’interface utilisateur de la visionneuse sont stylisés à l’aide d’illustrations bitmap et présentent plusieurs états visuels distincts. Un bon exemple est un bouton qui possède normalement au moins trois états différents : « up », « over » (supérieur), et « down » (inférieur). Chaque état nécessite l’attribution de sa propre illustration bitmap.

Avec une approche classique du style, le CSS dispose d’une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de CSS pour le style du bouton de zoom avant :

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

L’inconvénient de cette approche est que l’utilisateur final fait face à un scintillement ou à un retard de réponse de l’interface utilisateur lors de la première interaction avec l’élément. Cette action se produit, car l’illustration de l’image du nouvel état de l’élément n’a pas encore été téléchargée. En outre, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

CSS sprites est une approche différente où l’illustration d’image pour tous les états d’élément est combinée dans un seul fichier PNG appelé « sprite ». Ce « sprite » possède tous les états visuels pour l&#39;élément donné positionnés les uns à la suite des autres. Lors de la mise en forme d’un élément de l’interface utilisateur avec des sprites, la même image sprite est référencée pour tous les différents états dans le CSS. En outre, la propriété `background-position` est utilisée pour chaque état afin de spécifier quelle partie de l’image « sprite » est utilisée. Vous pouvez structurer une image « sprite » de n’importe quelle manière appropriée. Les visionneuses l’ont normalement empilé verticalement. Vous trouverez ci-dessous un exemple basé sur « sprite » de mise en forme du même bouton de zoom avant ci-dessus :

```
.s7basiczoomviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Notes et conseils généraux sur le style {#section-95855dccbbc444e79970f1aaa3260b7b}

* Lors de la personnalisation de l’interface utilisateur de la visionneuse avec CSS, l’utilisation de la règle `!IMPORTANT` n’est pas prise en charge pour appliquer un style aux éléments de la visionneuse. En particulier, `!IMPORTANT` règle ne doit pas être utilisée pour remplacer un style par défaut ou au moment de l’exécution fourni par la visionneuse ou le SDK de la visionneuse. En effet, cela peut affecter le comportement des composants appropriés. À la place, vous devez utiliser des sélecteurs CSS avec la spécificité appropriée pour définir les propriétés CSS qui sont documentées dans ce guide de référence.
* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS, et non par rapport à l’emplacement de la page HTML de la visionneuse. Tenez compte de cette règle lorsque vous copiez le CSS par défaut vers un autre emplacement. Copiez également les ressources par défaut ou mettez à jour les chemins d’accès dans le fichier CSS personnalisé.
* Le format préféré pour les illustrations bitmap est PNG.
* L’illustration bitmap est affectée aux éléments de l’interface utilisateur à l’aide de la propriété `background-image`.
* Les propriétés `width` et `height` d’un élément de l’interface utilisateur définissent sa taille logique. La taille de l’image bitmap transmise à `background-image` n’affecte pas la taille logique.
* Pour utiliser la densité élevée en pixels des écrans haute résolution tels que Retina, spécifiez une illustration bitmap deux fois plus grande que la taille de l’élément de l’interface utilisateur logique. Appliquez ensuite la propriété `-webkit-background-size:contain` pour réduire l’arrière-plan à la taille de l’élément logique de l’interface utilisateur.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` à sa classe CSS.
* Vous pouvez utiliser différents formats pour les valeurs de couleur prises en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

## Éléments courants de l’interface utilisateur {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici la documentation de référence sur les éléments de l’interface utilisateur qui s’applique à la visionneuse Zoom de base :
