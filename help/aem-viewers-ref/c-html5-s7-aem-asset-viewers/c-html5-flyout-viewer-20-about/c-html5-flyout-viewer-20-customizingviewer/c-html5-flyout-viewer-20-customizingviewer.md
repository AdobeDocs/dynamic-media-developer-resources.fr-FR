---
description: 'null'
keywords: responsive
seo-description: 'null'
seo-title: Personnalisation de la visionneuse Fenêtre déroulante
solution: Experience Manager
title: Personnalisation de la visionneuse Fenêtre déroulante
topic: Dynamic media
uuid: 10b5caa4-5298-43fa-af86-4f0b77be967b
translation-type: tm+mt
source-git-commit: 8d7fdab78c5d23d0e541effa9b9c470921bd144b

---


# Personnalisation de la visionneuse Fenêtre déroulante{#customizing-flyout-viewer}

Toutes les personnalisations visuelles et la plupart des personnalisations de comportement sont effectuées en créant une page CSS personnalisée.

Le flux de travail suggéré consiste à extraire le fichier CSS par défaut pour la visionneuse appropriée, à le copier vers un autre emplacement, à le personnaliser et à spécifier l’emplacement du fichier personnalisé dans la `style=` commande.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/FlyoutViewer.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que les déclarations par défaut. Si une déclaration de classe est omise, le lecteur ne fonctionne pas correctement car il ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Vous pouvez également fournir des règles CSS personnalisées en utilisant des styles incorporés directement sur la page Web ou dans l’une des règles CSS externes liées.

Lors de la création d’une page CSS personnalisée, gardez à l’esprit que le lecteur affecte `.s7flyoutviewer` une classe à son élément DOM . Si vous utilisez un fichier CSS externe transmis avec `style=` la commande, utilisez `.s7flyoutviewer` class comme classe parent dans le sélecteur descendant pour vos règles CSS. Si vous créez des styles intégrés sur la page Web, qualifiez en outre ce sélecteur avec l’ID de l’élément DOM  comme suit :

`#<containerId>.s7flyoutviewer`

## Création de CSS adaptés {#section-c1e74f5114ad418884ca1c95f5ea5b63}

Il est possible d’de différents périphériques et de différentes tailles d’incorporation dans une page CSS afin de rendre votre contenu affiché différemment, selon le périphérique de l’utilisateur ou une disposition de page Web particulière. Cela inclut, entre autres, les différentes mises en page de pages Web, la taille des éléments de l’interface utilisateur et la résolution des illustrations.

Le lecteur de contenu prend en charge deux méthodes pour créer une page CSS adaptée : Marqueurs CSS et  de média CSS standard. Vous pouvez utiliser ces méthodes indépendamment ou ensemble.

**Marqueurs CSS**

Pour faciliter la création d’une page CSS adaptée, le lecteur prend en charge les marqueurs CSS attribués dynamiquement aux classes CSS spéciales à l’élément de de la visionneuse de niveau supérieur en fonction de la taille de la visionneuse d’exécution et du type d’entrée utilisé sur le périphérique actuel.

Le premier groupe de marqueurs CSS comprend `.s7size_large`, `.s7size_medium`et `.s7size_small` des classes. Elles sont appliquées en fonction de la zone d’exécution du  du lecteur de contenu. En d’autres termes, si la zone du lecteur est égale ou supérieure à la taille d’un moniteur de bureau commun `.s7size_large` est utilisée; si la zone est proche de la taille d’une tablette commune `.s7size_medium` est affectée. Pour les zones similaires aux écrans de téléphone mobile `.s7size_small` est définie. L’objectif principal de ces marqueurs CSS est de créer différentes mises en page d’interface utilisateur pour différents écrans et tailles de visionneuse.

Le deuxième groupe de marqueurs CSS comprend `.s7mouseinput` et `.s7touchinput`. `.s7touchinput` est définie si le périphérique actif dispose de fonctionnalités d’entrée tactile ; dans le cas contraire, `.s7mouseinput` est utilisée. Ces marqueurs sont destinés à créer des éléments d’entrée de l’interface utilisateur avec des tailles d’écran différentes pour différents types d’entrée, car la saisie tactile requiert normalement des éléments plus volumineux. Si le périphérique dispose de fonctionnalités tactiles et d’entrée de souris, `.s7touchinput` est défini et le lecteur effectue le rendu d’une interface utilisateur tactile.

L’exemple CSS suivant définit la taille du bouton de zoom sur 28 x 28 pixels sur les systèmes avec saisie de la souris et 56 x 56 pixels sur les périphériques tactiles. En outre, il masque complètement le bouton si la taille du lecteur devient vraiment petite :

```
.s7flyoutviewer.s7mouseinput .s7swatches .s7thumb {  
 width: 28px; 
 height: 28px; 
} 
.s7flyoutviewer.s7touchinput .s7swatches .s7thumb {  
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer.s7size_small .s7swatches {  
 visibility: hidden; 
}
```

Pour des périphériques avec une densité de pixels différente, utilisez le de médias CSS. Le bloc de multimédia suivant contiendra des feuilles CSS spécifiques aux écrans haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation des marqueurs CSS est la méthode la plus souple pour créer des feuilles CSS adaptées qui vous permettent de  non seulement la taille de l’écran du périphérique, mais aussi la taille réelle du lecteur, ce qui peut s’avérer utile pour les mises en page de pages Web adaptées.

**de médias CSS**

La détection de périphérique peut également être réalisée à l’aide de  de média CSS purs. Tout ce qui est contenu dans un bloc de de médias donné est appliqué uniquement lorsqu&#39;il est exécuté sur un périphérique correspondant.

Lorsqu’il est appliqué aux visionneuses mobiles, utilisez quatre  de médias CSS, définis dans votre page CSS dans l’ordre suivant :

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

À l’aide d’une approche  média, vous devez organiser les feuilles de style CSS avec la détection de périphérique comme suit :

* Tout d’abord, la section spécifique au bureau définit toutes les propriétés propres au bureau ou communes à tous les écrans.
* Ensuite, les quatre de médias suivent l’ordre défini ci-dessus et fournissent des règles CSS spécifiques au type de périphérique correspondant.

Il n’est pas nécessaire d’ l’intégralité du fichier CSS du lecteur dans chaque  de média. Seules les propriétés spécifiques à des périphériques donnés sont redéfinies dans un multimédia.

## Sprites CSS {#section-0711ece44a4740168cfd7624c9010bd1}

De nombreux éléments de l’interface utilisateur du lecteur sont mis en forme à l’aide d’illustrations bitmap et présentent plusieurs états visuels distincts. Un bon exemple est un bouton qui a normalement 3 états différents : &quot;up&quot;, &quot;over&quot; et &quot;down&quot;. Chaque état requiert l’attribution de sa propre illustration bitmap.

Avec une approche classique de la mise en forme, le fichier CSS aurait une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de page CSS pour la mise en forme du bouton de défilement :

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-image:url(images/v2/ScrollLeftButton_up.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-image:url(images/v2/ScrollLeftButton_down.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-image:url(images/v2/ScrollLeftButton_disabled.png);  
}
```

L’inconvénient de cette approche est que l’utilisateur final subit un scintillement ou une réponse différée de l’interface utilisateur lors de la première interaction de l’élément. Cette action se produit car l’illustration de l’image pour le nouvel état de l’élément n’est pas encore téléchargée. De plus, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

Les images-objets CSS sont une approche différente, où les illustrations d’image pour tous les états d’élément sont combinées dans un fichier PNG unique appelé &quot;image-objet&quot;. Un tel &quot;sprite&quot; a tous les états visuels pour l’élément donné positionné l’un après l’autre. Lors de la mise en forme d’un élément d’interface utilisateur avec des images-objets, la même image-objet est référencée pour tous les états différents du CSS. En outre, la `background-position` propriété est utilisée pour chaque état pour spécifier la partie de l’image &quot;sprite&quot; utilisée. Vous pouvez structurer une image &quot;sprite&quot; de n’importe quelle manière appropriée. Les lecteurs disposent normalement d’un empilement vertical. Vous trouverez ci-dessous un exemple de style basé sur des &quot;images-objets&quot; du même bouton de défilement depuis le haut :

```
.s7flyoutviewer .s7scrollleftbutton[state]  { 
    background-image: url(images/v2/ScrollLeftButton_light_sprite.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-position: -56px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-position: -0px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-position: -56px -448px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-position: -0px -448px;  
}
```

## Notes et conseils de mise en forme générale {#section-95855dccbbc444e79970f1aaa3260b7b}

* Lors de la personnalisation de l’interface utilisateur du lecteur avec CSS, l’utilisation de la `!IMPORTANT` règle n’est pas prise en charge pour mettre en forme les éléments du lecteur. En particulier, `!IMPORTANT` la règle ne doit pas être utilisée pour remplacer le style par défaut ou d’exécution fourni par le lecteur ou le kit de développement de visionneuse. La raison en est qu&#39;elle peut affecter le comportement des composants appropriés. Utilisez plutôt des sélecteurs CSS avec la spécificité appropriée pour définir les propriétés CSS documentées dans ce guide de référence.
* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS et non par rapport à l’emplacement de la page HTML de la visionneuse. Tenez compte de cette règle lorsque vous copiez le fichier CSS par défaut vers un autre emplacement. Copiez également les ressources par défaut ou mettez à jour les chemins d’accès dans le fichier CSS personnalisé.
* Le format préféré pour les illustrations bitmap est le format PNG.
* Les illustrations bitmap sont affectées aux éléments de l’interface utilisateur à l’aide de la `background-image` propriété.
* Les propriétés `width` et `height` les propriétés d’un élément d’interface utilisateur définissent sa taille logique. La taille du bitmap transmis à `background-image` n’affecte pas la taille logique.
* Pour utiliser la haute densité de pixels des écrans haute résolution comme Retina, spécifiez une illustration bitmap deux fois plus grande que la taille d’élément logique de l’interface utilisateur. Ensuite, appliquez la `-webkit-background-size:contain` propriété pour réduire l’arrière-plan à la taille de l’élément logique de l’interface utilisateur.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` à sa classe CSS.
* Vous pouvez utiliser divers formats pour la valeur de couleur prise en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

## Éléments communs de l’interface utilisateur {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici la documentation de référence sur les éléments de l’interface utilisateur qui s’applique à la visionneuse Fenêtre déroulante :

* [de zoom déroulant](r-html5-flyout-viewer-20-customize-flyoutzoomview.md)
* [Mise en valeur](r-html5-flyout-viewer-20-customize-focushighlight.md)
* [Zone du lecteur principal](r-html5-flyout-viewer-20-customize-mainviewerarea.md)
* [Echantillons](r-html5-flyout-viewer-20-customize-swatches.md)
* [Info-bulles](r-html5-flyout-viewer-20-customize-tooltips.md)
