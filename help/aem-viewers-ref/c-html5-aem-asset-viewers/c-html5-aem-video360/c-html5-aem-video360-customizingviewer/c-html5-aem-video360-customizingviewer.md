---
title: Personnalisation de la visionneuse Video360
description: Toute la personnalisation visuelle et la plupart des personnalisations de comportement pour la visionneuse Video360 s’effectuent en créant un CSS personnalisé.
keywords: sensible
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '1295'
ht-degree: 0%

---

# Personnalisation de la visionneuse Video360{#customizing-video-viewer}

Toute la personnalisation visuelle et la plupart des personnalisations de comportement pour la visionneuse Video360 s’effectuent en créant un CSS personnalisé.

Le flux de travail suggéré consiste à prendre le fichier CSS par défaut pour la visionneuse appropriée, à le copier dans un emplacement différent, à le personnaliser et à spécifier l’emplacement du fichier personnalisé dans la `style=` commande.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/Video360Viewer_dark.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que le fichier par défaut. Si une déclaration de classe est omise, la visionneuse ne fonctionne pas correctement car elle ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre façon de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement sur la page Web ou dans l’une des règles CSS externes liées.

Lorsque vous créez une feuille CSS personnalisée, n’oubliez pas que la visionneuse attribue une `.s7video360viewer` classe à son élément DOM conteneur. Si vous utilisez un fichier CSS externe transmis avec `style=` la commande, utilisez `.s7video360viewer` la classe comme classe parent dans le sélecteur de descendants de vos règles CSS. Si vous utilisez des styles incorporés sur la page Web, qualifiez également ce sélecteur avec un ID de l’élément DOM conteneur comme suit :

`#<containerId>.s7video360viewer`

## Création d’une feuille CSS responsive conçue {#section-0bb49aca42d242d9b01879d5ba59d33b}

Il est possible de cibler différents appareils et tailles d’intégration dans CSS pour que votre contenu s’affiche différemment en fonction de l’appareil d’un utilisateur ou d’une mise en page Web particulière. Cette méthode inclut, mais sans s’y limiter, différentes dispositions, tailles d’éléments d’interface utilisateur et résolution d’illustration.

La visionneuse prend en charge deux mécanismes de création de CSS conçus en responsive design : les marqueurs CSS et les requêtes multimédias CSS standard. Vous pouvez utiliser des marqueurs ou des requêtes indépendamment ou ensemble.

**Marqueurs CSS**

Pour faciliter la création d’une feuille CSS adaptée, la visionneuse prend en charge les marqueurs CSS. Ces marqueurs sont des classes CSS spéciales qui sont attribuées dynamiquement à l’élément conteneur de visionneuse de niveau supérieur. Ils sont basés sur la taille de la visionneuse d’exécution et le type d’entrée utilisé sur le périphérique actuel.

Le premier groupe de marqueurs CSS comprend `.s7size_large`, `.s7size_medium`et `.s7size_small` les classes. Ils sont appliqués en fonction de la zone d’exécution du conteneur de la visionneuse. Si la zone de visionneuse est égale ou supérieure à la taille d’un moniteur de bureau commun, est `.s7size_large` utilisée ; si la zone est proche d’une tablette commune, elle `.s7size_medium` est affectée. Pour les zones similaires aux écrans de téléphone mobile, alors `.s7size_small` est défini. L’objectif principal de ces marqueurs CSS est de créer différentes dispositions d’interface utilisateur pour différents écrans et tailles de visionneuses.

Le deuxième groupe de marqueurs CSS contient `.s7mouseinput` et `.s7touchinput`. Le marqueur `.s7touchinput` est défini si le périphérique actuel dispose de capacités d’entrée tactile ; sinon, `.s7mouseinput` est utilisé. Ces marqueurs sont principalement destinés à créer des éléments d’entrée d’interface utilisateur avec différentes tailles d’écran pour différents types d’entrée, car normalement l’entrée tactile nécessite des éléments plus grands. Dans le cas où l’appareil dispose à la fois de capacités d’entrée de souris et tactiles, `.s7touchinput` est défini et le spectateur rend une interface utilisateur tactile.

L’exemple de CSS suivant définit la taille du bouton lecture/pause sur 28x28 pixels sur les systèmes avec entrée souris et 56x56 pixels sur les périphériques tactiles. De plus, le bouton est complètement masqué si la taille de la visionneuse est réduite de manière significative :

```
.s7video360viewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7video360viewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7video360viewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Pour cibler des appareils avec une densité de pixels différente, vous devez utiliser des requêtes de média CSS. Le bloc de requête de média suivant contiendrait un code CSS spécifique aux écrans haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation de marqueurs CSS est le moyen le plus flexible de créer des CSS conçus en responsive design, car ils vous permettent de cibler non seulement la taille de l’écran de l’appareil, mais aussi la taille réelle de la visionneuse, ce qui est utile pour les mises en page de conception réactive.

Vous pouvez utiliser le fichier CSS de visionneuse par défaut comme exemple d’approche de marqueurs CSS.

**Requêtes de média CSS**

Vous pouvez également effectuer la détection de périphérique à l’aide de requêtes de média CSS pures. Tout ce qui est inclus dans un bloc de requête de média donné n’est appliqué que lorsqu’il est exécuté sur un périphérique correspondant.

Lorsqu’elles sont appliquées à des applications HTML5, les visionneuses mobiles utilisent quatre requêtes de média CSS, définies dans votre fichier CSS, dans l’ordre indiqué ci-dessous :

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

En utilisant une approche de requêtes de média, vous devez organiser CSS avec la détection de périphérique comme suit :

* Tout d’abord, la section spécifique au bureau définit toutes les propriétés spécifiques au bureau ou communes à tous les écrans.
* Et deuxièmement, les quatre requêtes de média vont dans l’ordre défini ci-dessus et fournissent des règles CSS spécifiques au type d’appareil correspondant.

Il n’est pas nécessaire de dupliquer l’intégralité du fichier CSS de la visionneuse dans chaque requête de média. Seules les propriétés spécifiques à des périphériques donnés sont redéfinies dans une requête de média.

## CSS Sprites {#section-9b6d8d601cb441d08214dada7bb4eddc}

De nombreux éléments de l’interface utilisateur de la visionneuse sont stylisés à l’aide d’illustrations bitmap et ont plusieurs états visuels distincts. Un bon exemple est un bouton qui a normalement au moins trois états différents : « haut », « au-dessus » et « bas ». Chaque état requiert l’affectation d’une illustration bitmap.

Avec une approche classique du style, le CSS aurait une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de CSS pour appliquer un style à un bouton Plein écran :

```
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

L’inconvénient de cette approche est que l’utilisateur final rencontre une réponse scintillante ou retardée de l’interface utilisateur lorsque l’élément est interagi avec pour la première fois. Cette action se produit car l’illustration d’image pour le nouvel état d’élément n’est pas encore téléchargée. En outre, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

CSS sprites est une approche différente où l’illustration d’image pour tous les états d’élément est combinée dans un seul fichier PNG appelé « sprite ». Un tel « sprite » a tous les états visuels de l’élément donné positionnés les uns après les autres. Lors du style d’un élément d’interface utilisateur avec des sprites, la même image de sprite est référencée pour tous les différents états dans le CSS. En outre, la `background-position` propriété est utilisée pour chaque état afin de spécifier quelle partie de l’image « sprite » est utilisée. Vous pouvez structurer une image « sprite » de n’importe quelle manière appropriée. Les téléspectateurs l’ont normalement empilé verticalement. Voici un exemple basé sur « sprite » de style du même bouton plein écran précédemment :

```
.s7video360viewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Notes générales de style et conseils {#section-95855dccbbc444e79970f1aaa3260b7b}

* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS, et non à l’emplacement de la page HTML de la visionneuse. Tenez compte de cette règle lorsque vous copiez le fichier CSS par défaut vers un autre emplacement. Copiez également les ressources par défaut ou mettez à jour les chemins d’accès dans la feuille CSS personnalisée.
* Le format préféré pour les illustrations bitmap est PNG.
* L’illustration bitmap est affectée aux éléments de l’interface utilisateur à l’aide de la `background-image` propriété.
* Les `width` propriétés et `height` d’un élément d’interface utilisateur définissent sa taille logique. La taille du bitmap transmis à `background-image` n’affecte pas la taille logique.

* Pour utiliser la densité de pixels élevée des écrans haute résolution tels que Retina, spécifiez une illustration bitmap deux fois plus grande que la taille de l’élément de l’interface utilisateur logique. Ensuite, appliquez la `-webkit-background-size:contain` propriété pour réduire l’arrière-plan à la taille de l’élément de l’interface utilisateur logique.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` un bouton à sa classe CSS.
* Vous pouvez utiliser différents formats de valeurs colorimétriques pris en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

* Lors de la personnalisation de l’interface utilisateur de la visionneuse avec CSS, l’utilisation de la règle n’est pas prise en charge pour mettre en `!IMPORTANT` forme les éléments de la visionneuse. En particulier, `!IMPORTANT` la règle ne doit pas être utilisée pour remplacer un style par défaut ou d’exécution fourni par la visionneuse ou le Kit de développement logiciel (SDK) de la visionneuse. La raison en est que cela peut affecter le comportement des composants appropriés. Au lieu de cela, vous devez utiliser des sélecteurs CSS avec la spécificité appropriée pour définir les propriétés CSS qui sont documentées dans ce guide de référence.

## Éléments courants de l’interface utilisateur {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici la documentation de référence des éléments d’interface utilisateur qui s’applique à la visionneuse Video360 :
