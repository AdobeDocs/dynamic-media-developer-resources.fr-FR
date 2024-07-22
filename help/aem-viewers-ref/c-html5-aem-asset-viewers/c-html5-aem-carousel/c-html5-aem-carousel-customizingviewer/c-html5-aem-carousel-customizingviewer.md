---
title: Personnalisation de la visionneuse de carrousel
description: Toutes les personnalisations visuelles et la plupart des personnalisations de comportement pour la visionneuse de carrousel sont effectuées par la création d’une page CSS personnalisée.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f392d830-5c75-45dd-bab8-29a38218790d
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 0%

---

# Personnalisation de la visionneuse de carrousel{#customizing-carousel-viewer}

Toutes les personnalisations visuelles et la plupart des personnalisations de comportement pour la visionneuse de carrousel sont effectuées par la création d’une page CSS personnalisée.

Le workflow suggéré consiste à prendre le fichier CSS par défaut pour la visionneuse appropriée, à le copier vers un autre emplacement, à le personnaliser, et à spécifier l’emplacement du fichier personnalisé dans la commande `style=`.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/CarouselViewer_dotted_light.css`

La visionneuse est fournie avec quatre fichiers CSS prêts à l’emploi, pour les indicateurs d’ensemble numériques et en pointillés, chacun dans un jeu de couleurs &quot;clair&quot; et &quot;foncé&quot;. La version &quot;Dotted light&quot; est utilisée par défaut, mais il est facile de passer à une autre version à l’aide d’un autre CSS standard et de définir le paramètre `SetIndicator.mode` . D’autres CSS standard se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/CarouselViewer_dotted_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_light.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que celles par défaut. Si une déclaration de classe est omise, la visionneuse ne fonctionne pas correctement, car elle ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre manière de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement sur la page web ou dans l’une des règles CSS externes liées.

Lors de la création d’une page CSS personnalisée, gardez à l’esprit que la visionneuse affecte la classe `.s7carouselviewer` à son élément DOM de conteneur. Si vous utilisez un fichier CSS externe transmis avec la commande `style=`, utilisez la classe `.s7carouselviewer` comme classe parente dans le sélecteur descendant pour vos règles CSS. Si vous ajoutez des styles intégrés à la page web, qualifiez également ce sélecteur avec un identifiant de l’élément DOM du conteneur comme suit :

`#<containerId>.s7carouselviewer`

## Création d’une page CSS adaptée {#section-0bb49aca42d242d9b01879d5ba59d33b}

Il est possible de cibler différents appareils et d’incorporer des tailles différentes dans une feuille CSS afin de rendre l’affichage de votre contenu différent, en fonction de l’appareil d’un utilisateur ou d’une mise en page web spécifique. Cette technique comprend, sans s’y limiter, différentes mises en page, tailles d’éléments de l’interface utilisateur et résolution des illustrations.

La visionneuse prend en charge deux mécanismes de création de CSS responsive design : les marqueurs CSS et les requêtes multimédias CSS standard. Vous pouvez utiliser ces deux mécanismes séparément ou ensemble.

**Marqueurs CSS**

Pour faciliter la création de CSS responsive design, la visionneuse prend en charge les marqueurs CSS. Ces marqueurs sont des classes CSS spéciales qui sont attribuées dynamiquement à l’élément de conteneur de visionneuse de niveau supérieur. Elles sont basées sur la taille de la visionneuse d’exécution et le type d’entrée utilisé sur l’appareil actuel.

Le premier groupe de marqueurs CSS contient les classes `.s7size_large`, `.s7size_medium` et `.s7size_small`. Elles sont appliquées en fonction de la zone d’exécution du conteneur de la visionneuse. Par exemple, si la zone de visionneuse est égale ou supérieure à la taille d’un écran de bureau commun, utilisez `.s7size_large`. Si la zone est proche d’un périphérique tablette commun, affectez `.s7size_medium`. Pour les zones similaires aux écrans de téléphone mobile, utilisez `.s7size_small`. L’objectif principal de ces marqueurs CSS est de créer différentes mises en page d’interface utilisateur pour différents écrans et tailles de visionneuse.

Le deuxième groupe de marqueurs CSS contient `.s7mouseinput` et `.s7touchinput`. Le marqueur CSS `.s7touchinput` est défini si l’appareil actuel est une entrée tactile. Sinon, `.s7mouseinput` est utilisé. Ces marqueurs sont principalement destinés à créer des éléments d’entrée de l’interface utilisateur avec des tailles d’écran différentes pour différents types d’entrée, car la saisie tactile nécessite normalement des éléments plus volumineux.

L’exemple de page CSS suivant définit la taille du bouton de zoom sur 28 x 28 pixels sur les systèmes avec une entrée de souris et sur 56 x 56 pixels sur les périphériques d’entrée tactile. Si la taille de la visionneuse est encore plus petite, elle est définie sur 20 x 20 pixels.

```
.s7carouselviewer.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7carouselviewer.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7carouselviewer.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
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

**Requêtes multimédias CSS**

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

## sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

De nombreux éléments de l’interface utilisateur de la visionneuse sont stylisés à l’aide d’illustrations bitmap et possèdent plusieurs états visuels distincts. Un bon exemple est un bouton qui a normalement au moins trois états différents : `up`, `over` et `down`. Chaque état nécessite l’attribution de sa propre illustration bitmap.

Avec une approche classique du style, le CSS possède une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de page CSS permettant de mettre en forme un bouton de zoom avant :

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

L’inconvénient de cette approche est que l’utilisateur final subit un scintillement ou une réponse de l’interface utilisateur différée lorsque l’élément est interagi pour la première fois. Cette action se produit car l’illustration de l’image pour le nouvel état d’élément n’est pas encore téléchargée. En outre, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

Les sprites CSS constituent une approche différente selon laquelle l’illustration d’image pour tous les états d’élément est combinée dans un seul fichier PNG appelé &quot;sprite&quot;. Un tel &quot;sprite&quot; a tous les états visuels pour l’élément donné positionnés l’un après l’autre. Lors du style d’un élément d’interface utilisateur avec des sprites, la même image de sprite est référencée pour tous les états différents du CSS. En outre, la propriété `background-position` est utilisée pour chaque état pour spécifier la partie de l’image &quot;sprite&quot; utilisée. Vous pouvez structurer une image &quot;sprite&quot; de n’importe quelle manière appropriée. Les visionneuses disposent normalement d’un empilement vertical.

Voici un exemple de style basé sur un &quot;sprite&quot; de la même icône de zone réactive :

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## Notes et conseils généraux sur le style {#section-95855dccbbc444e79970f1aaa3260b7b}

* Lors de la personnalisation de l’interface utilisateur de la visionneuse avec CSS, l’utilisation de la règle `!IMPORTANT` n’est pas prise en charge pour appliquer un style aux éléments de la visionneuse. En particulier, la règle `!IMPORTANT` ne doit pas être utilisée pour remplacer le style par défaut ou d’exécution fourni par la visionneuse ou le SDK de la visionneuse. La raison en est qu’elle peut affecter le comportement des composants appropriés. Vous devez plutôt utiliser des sélecteurs CSS avec la précision appropriée pour définir les propriétés CSS documentées dans ce guide de référence des visionneuses.
* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS, et non par rapport à l’emplacement de la page d’HTML de la visionneuse. Tenez compte de cette règle lorsque vous copiez le CSS par défaut vers un autre emplacement. Copiez également les ressources par défaut ou mettez à jour tous les chemins d’accès dans le CSS personnalisé.
* Le format préféré des illustrations bitmap est PNG.
* L’illustration bitmap est affectée aux éléments de l’interface utilisateur à l’aide de la propriété `background-image`.
* Les propriétés `width` et `height` d’un élément d’interface utilisateur définissent sa taille logique. La taille de l’image bitmap transmise à `background-image` n’affecte pas sa taille logique.
* Pour utiliser la haute densité en pixels d’écrans haute résolution comme Retina, spécifiez une illustration bitmap deux fois plus grande que la taille de l’élément logique de l’interface utilisateur. Ensuite, appliquez la propriété `-webkit-background-size:contain` pour réduire l’arrière-plan à la taille de l’élément logique de l’interface utilisateur.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` à sa classe CSS.
* Vous pouvez utiliser différents formats pour la valeur de couleur prise en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

## Éléments d’interface utilisateur courants {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici la documentation de référence sur les éléments de l’interface utilisateur qui s’applique à la visionneuse d’images vidéo :
