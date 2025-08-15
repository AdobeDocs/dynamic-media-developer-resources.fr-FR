---
title: Personnalisation de la visionneuse à 360°
description: Toutes les personnalisations visuelles et la plupart des personnalisations comportementales de la visionneuse à 360° sont effectuées en créant un fichier CSS personnalisé.
keywords: réactif
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: eb2ad4ee-933f-408d-955e-be9bb7484192
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 0%

---

# Personnalisation de la visionneuse à 360°{#customizing-spin-viewer}

Toutes les personnalisations visuelles et la plupart des personnalisations comportementales de la visionneuse à 360° sont effectuées en créant un fichier CSS personnalisé.

Le flux de travail suggéré consiste à prendre le fichier CSS par défaut pour la visionneuse appropriée, à le copier dans un emplacement différent, à le personnaliser et à spécifier l’emplacement du fichier personnalisé dans la `style=` commande.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/SpinViewer_light.css`

La visionneuse est fournie avec des fichiers CSS prêts à l’emploi, pour les couleurs « claires » et « sombres ». La version « claire » est utilisée par défaut, mais vous pouvez passer à la version « sombre » en utilisant le CSS standard suivant :

`<s7_viewers_root>/html5/SpinViewer_dark.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que le fichier par défaut. Si une déclaration de classe est omise, la visionneuse ne fonctionne pas correctement car elle ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre manière de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement dans la page web ou dans l’une des règles CSS externes liées.

Lors de la création d’un CSS personnalisé, gardez à l’esprit que la visionneuse attribue `.s7spinviewer` classe à son élément DOM conteneur. Si vous utilisez un fichier CSS externe transmis avec `style=` commande, utilisez `.s7spinviewer` classe comme classe parente dans le sélecteur descendant pour vos règles CSS. Si vous utilisez des styles incorporés sur la page Web, qualifiez également ce sélecteur avec un ID de l’élément DOM conteneur comme suit :

`#<containerId>.s7spinviewer`

## Création d’une feuille CSS responsive conçue {#section-0bb49aca42d242d9b01879d5ba59d33b}

Il est possible de cibler différents appareils et tailles d’intégration dans CSS pour que votre contenu s’affiche différemment, en fonction de l’appareil d’un utilisateur ou d’une mise en page Web particulière. Cette capacité inclut, mais sans s’y limiter, différentes mises en page Web, tailles d’éléments d’interface utilisateur et résolution d’illustration.

La visionneuse prend en charge deux méthodes pour créer un CSS réactif : les marqueurs CSS et les requêtes de média CSS standard. Vous pouvez utiliser ces méthodes séparément ou ensemble.

**Marqueurs CSS**

Pour vous aider à créer une feuille de style CSS en responsive design, la visionneuse prend en charge les marqueurs CSS qui des classes CSS spéciales sont affectées dynamiquement à l’élément de conteneur de visionneuse de niveau supérieur. Ces classes sont basées sur la taille de la visionneuse au moment de l’exécution et le type d’entrée utilisé sur l’appareil actuel.

Le premier groupe de marqueurs CSS comprend les classes `.s7size_large`, `.s7size_medium` et `.s7size_small`. Elles sont appliquées en fonction de la zone d’exécution du conteneur de la visionneuse. En d’autres termes, si la zone de la visionneuse est égale ou supérieure à la taille d’un moniteur de bureau commun `.s7size_large` est utilisé, et si la zone est proche de la taille d’une tablette commune, `.s7size_medium` est attribué. Pour les zones similaires aux écrans de téléphone mobile, `.s7size_small` est définie. L’objectif principal de ces marqueurs CSS est de créer différentes dispositions d’interface utilisateur pour différents écrans et tailles de visionneuses.

Le deuxième groupe de marqueurs CSS comprend `.s7mouseinput` et `.s7touchinput`. Le marqueur `.s7touchinput` est défini si l’appareil actuel dispose de fonctionnalités d’entrée tactile ; dans le cas contraire, `.s7mouseinput` est utilisé. Ces marqueurs sont destinés à créer des éléments d’entrée de l’interface utilisateur avec différentes tailles d’écran pour différents types d’entrée, car normalement l’entrée tactile nécessite des éléments plus grands. Si l’appareil dispose à la fois des fonctionnalités d’entrée de souris et tactiles, `.s7touchinput` est défini et la visionneuse offre une interface utilisateur conviviale pour les écrans tactiles.

L’exemple de CSS suivant définit la taille du bouton de zoom avant sur 28 x 28 pixels sur les systèmes dotés d’une entrée de souris et 56 x 56 pixels sur les appareils tactiles. En outre, le bouton est complètement masqué si la taille de la visionneuse devient réduite :

```
.s7spinviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7spinviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7spinviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Pour cibler des périphériques avec une densité de pixels différente, utilisez des requêtes de média CSS. Le bloc de requête de média suivant contiendrait un code CSS spécifique aux écrans haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation de marqueurs CSS est le moyen le plus flexible de créer des CSS conçus en responsive design. La raison en est qu’il vous permet de cibler non seulement la taille de l’écran de l’appareil, mais aussi la taille réelle de la visionneuse, ce qui peut être utile pour les mises en page de conception réactive.

Utilisez le fichier CSS de la visionneuse par défaut comme exemple d’approche de marqueurs CSS.

**Requêtes de média CSS**

La détection des périphériques peut également être effectuée à l’aide de requêtes de média CSS pures. Tous les éléments inclus dans un bloc de requête de média donné sont appliqués uniquement lorsqu’ils sont exécutés sur un appareil correspondant.

Lorsqu’elles sont appliquées aux visionneuses mobiles, utilisez quatre requêtes de média CSS, définies dans votre CSS dans l’ordre suivant :

1. Contient uniquement des règles spécifiques à tous les appareils tactiles.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. Contient uniquement des règles spécifiques pour les tablettes dotées d’écrans haute résolution.

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

1. Contient uniquement des règles spécifiques aux téléphones portables dotés d’écrans haute résolution.

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

## Sprites CSS {#section-b671c70acf284cb0aea678c2d2e4babc}

De nombreux éléments de l’interface utilisateur de la visionneuse sont stylisés à l’aide d’illustrations bitmap et ont plusieurs états visuels distincts. Un bon exemple est un bouton qui possède normalement au moins trois états différents : « up », « over » (supérieur), et « down » (inférieur). Chaque état nécessite l’attribution de sa propre illustration bitmap.

Avec une approche classique du style, le CSS dispose d’une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de CSS pour le style du bouton de zoom avant :

```
.s7spinviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

L’inconvénient de cette approche est que l’utilisateur final fait face à un scintillement ou à un retard de réponse de l’interface utilisateur lors de la première interaction avec l’élément. Cette action se produit, car l’illustration de l’image du nouvel état de l’élément n’a pas encore été téléchargée. En outre, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

CSS sprites est une approche différente où l’illustration d’image pour tous les états d’élément est combinée dans un seul fichier PNG appelé « sprite ». Ce « sprite » possède tous les états visuels pour l&#39;élément donné positionnés les uns à la suite des autres. Lors de la mise en forme d’un élément de l’interface utilisateur avec des sprites, la même image sprite est référencée pour tous les différents états dans le CSS. En outre, la `background-position` propriété est utilisée pour chaque état afin de spécifier quelle partie de l’image « sprite » est utilisée. Vous pouvez structurer une image « sprite » de n’importe quelle manière appropriée. Les téléspectateurs l’ont normalement empilé verticalement. Voici un exemple basé sur « sprite » d’un style du même bouton de zoom avant ci-dessus :

```
.s7spinviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Notes générales de style et conseils {#section-95855dccbbc444e79970f1aaa3260b7b}

* Lors de la personnalisation de l’interface utilisateur de la visionneuse avec CSS, l’utilisation de la règle `!IMPORTANT` n’est pas prise en charge pour appliquer un style aux éléments de la visionneuse. En particulier, `!IMPORTANT` règle ne doit pas être utilisée pour remplacer un style par défaut ou au moment de l’exécution fourni par la visionneuse ou le SDK de la visionneuse. En effet, cela peut affecter le comportement des composants appropriés. À la place, vous devez utiliser des sélecteurs CSS avec la spécificité appropriée pour définir les propriétés CSS qui sont documentées dans ce guide de référence.
* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS, et non par rapport à l’emplacement de la page HTML de la visionneuse. Tenez compte de cette règle lorsque vous copiez le CSS par défaut vers un autre emplacement. Copiez également les ressources par défaut ou mettez à jour les chemins d’accès dans le fichier CSS personnalisé.
* Le format préféré pour les illustrations bitmap est PNG.
* L’illustration bitmap est affectée aux éléments de l’interface utilisateur à l’aide de la `background-image` propriété.
* Les `width` propriétés et `height` d’un élément d’interface utilisateur définissent sa taille logique. La taille du bitmap transmis à `background-image` n’affecte pas la taille logique.
* Pour utiliser la densité élevée en pixels des écrans haute résolution tels que Retina, spécifiez une illustration bitmap deux fois plus grande que la taille de l’élément de l’interface utilisateur logique. Appliquez ensuite la propriété `-webkit-background-size:contain` pour réduire l’arrière-plan à la taille de l’élément logique de l’interface utilisateur.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` à sa classe CSS.
* Vous pouvez utiliser différents formats pour les valeurs de couleur prises en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

## Éléments courants de l’interface utilisateur {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici la documentation de référence des éléments de l’interface utilisateur qui s’applique à la visionneuse de supports variés :
