---
description: Toutes les personnalisations visuelles et la plupart des personnalisations de comportement pour la visionneuse de recherche de catalogue électronique sont effectuées par la création d’une page CSS personnalisée.
keywords: responsive
solution: Experience Manager
title: Personnalisation de la visionneuse de recherche de catalogue électronique
feature: Dynamic Media Classic,Visionneuses,SDK/API,Recherche catalogue électronique
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 0%

---

# Personnalisation de la visionneuse de recherche de catalogue électronique{#customizing-ecatalog-search-viewer}

Toutes les personnalisations visuelles et la plupart des personnalisations de comportement pour la visionneuse de recherche de catalogue électronique sont effectuées par la création d’une page CSS personnalisée.

Le workflow suggéré consiste à prendre le fichier CSS par défaut pour la visionneuse appropriée, à le copier vers un autre emplacement, à le personnaliser, et à spécifier l’emplacement du fichier personnalisé dans la commande `style=`.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que celles par défaut. Si une déclaration de classe est omise, la visionneuse ne fonctionne pas correctement, car elle ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre manière de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement sur la page web ou dans l’une des règles CSS externes liées.

Lors de la création d’une page CSS personnalisée, gardez à l’esprit que la visionneuse affecte la classe `.s7ecatalogsearchviewer` à son élément DOM de conteneur. Si vous utilisez un fichier CSS externe transmis avec la commande `style=`, utilisez la classe `.s7ecatalogsearchviewer` en tant que classe parente dans le sélecteur descendant pour vos règles CSS. Si vous effectuez des styles intégrés sur la page web, qualifiez en outre ce sélecteur avec un identifiant de l’élément DOM du conteneur comme suit :

`#<containerId>.s7ecatalogsearchviewer`

## Création d’une page CSS adaptée {#section-c1e74f5114ad418884ca1c95f5ea5b63}

Il est possible de cibler différents appareils et d’incorporer des tailles différentes dans une feuille CSS afin de rendre l’affichage de votre contenu différent, en fonction de l’appareil d’un utilisateur ou d’une mise en page web spécifique. Cela inclut, sans s’y limiter, différentes mises en page de pages web, tailles d’éléments de l’interface utilisateur et résolution des illustrations.

La visionneuse prend en charge deux méthodes pour créer une page CSS adaptée : Marqueurs CSS et requêtes multimédias CSS standard. Vous pouvez utiliser ces méthodes indépendamment ou ensemble.

**Marqueurs CSS**

Pour faciliter la création de CSS responsive design, la visionneuse prend en charge les marqueurs CSS qui sont des classes CSS spéciales dynamiquement affectées à l’élément de conteneur de la visionneuse de niveau supérieur en fonction de la taille de la visionneuse d’exécution et du type d’entrée utilisé sur l’appareil actuel.

Le premier groupe de marqueurs CSS comprend les classes `.s7size_large`, `.s7size_medium` et `.s7size_small`. Elles sont appliquées en fonction de la zone d’exécution du conteneur de la visionneuse. En d’autres termes, si la zone de visionneuse est égale ou supérieure à la taille d’un moniteur de bureau commun `.s7size_large` est utilisée ; si la zone est proche de la taille d’une tablette commune, la valeur `.s7size_medium` est affectée. Pour les zones semblables aux écrans de téléphone mobile, `.s7size_small` est défini. L’objectif Principal de ces marqueurs CSS est de créer différentes mises en page d’interface utilisateur pour différents écrans et tailles de visionneuse.

Le deuxième groupe de marqueurs CSS comprend `.s7mouseinput` et `.s7touchinput`. `.s7touchinput` est défini si l’appareil actuel dispose de fonctionnalités d’entrée tactile ; dans le cas contraire,  `.s7mouseinput` est utilisé. Ces marqueurs sont destinés à créer des éléments d’entrée de l’interface utilisateur avec des tailles d’écran différentes pour différents types d’entrée, car la saisie tactile nécessite normalement des éléments plus volumineux. Si l’appareil dispose de fonctionnalités d’entrée de souris et de tactile, `.s7touchinput` est défini et la visionneuse effectue le rendu d’une interface utilisateur tactile.

L’exemple de page CSS suivant définit la taille du bouton de zoom sur 28 x 28 pixels sur les systèmes avec saisie de la souris et 56 x 56 pixels sur les appareils tactiles. En outre, il masque complètement le bouton si la taille de la visionneuse devient vraiment réduite :

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7ecatalogsearchviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Pour cibler des appareils avec une densité de pixels différente, utilisez des requêtes multimédias CSS. Le bloc de requête multimédia suivant contiendrait une feuille CSS spécifique aux écrans à haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation de marqueurs CSS est la méthode la plus souple pour créer des CSS réactives, car elle vous permet de cibler non seulement la taille de l’écran de l’appareil, mais aussi la taille réelle de la visionneuse, ce qui peut s’avérer utile pour les mises en page réactives.

Utilisez le fichier CSS de visionneuse par défaut comme exemple d’approche des marqueurs CSS.

**Requêtes de média CSS**

La détection de périphérique peut également être effectuée à l’aide de requêtes multimédias CSS pures. Tout ce qui est inclus dans un bloc de requête multimédia donné est appliqué uniquement lorsqu’il est exécuté sur un appareil correspondant.

Lorsqu’elles sont appliquées aux visionneuses mobiles, utilisez quatre requêtes multimédias CSS, définies dans votre CSS dans l’ordre suivant :

1. Contient uniquement des règles spécifiques à tous les appareils tactiles.

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

À l’aide d’une approche de requêtes de média, vous devez organiser CSS avec la détection de périphérique comme suit :

* Tout d’abord, la section spécifique à l’ordinateur de bureau définit toutes les propriétés spécifiques à l’ordinateur ou communes à tous les écrans.
* Deuxièmement, les quatre requêtes de média suivent l’ordre défini ci-dessus et fournissent des règles CSS spécifiques au type d’appareil correspondant.

Il n’est pas nécessaire de dupliquer l’intégralité du CSS de la visionneuse dans chaque requête de média. Seules les propriétés spécifiques à des appareils donnés sont redéfinies au sein d’une requête multimédia.

## Sprites CSS {#section-9d570f95eb2443aca74c1b02f6e89aff}

De nombreux éléments de l’interface utilisateur de la visionneuse sont stylisés à l’aide d’illustrations bitmap et possèdent plusieurs états visuels distincts. Un bon exemple est un bouton qui comporte normalement au moins trois états différents : &quot;vers le haut&quot;, &quot;vers le bas&quot; et &quot;vers le bas&quot;. Chaque état nécessite l’attribution de sa propre illustration bitmap.

Avec une approche classique de la mise en forme, le CSS dispose d’une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de page CSS pour la mise en forme d’un bouton de zoom avant :

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

L’inconvénient de cette approche est que l’utilisateur final subit un scintillement ou une réponse de l’interface utilisateur différée lorsque l’élément est interagi pour la première fois. Cette action se produit car l’illustration de l’image pour le nouvel état d’élément n’est pas encore téléchargée. En outre, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

Les sprites CSS constituent une approche différente selon laquelle l’illustration d’image pour tous les états d’élément est combinée dans un seul fichier PNG appelé &quot;sprite&quot;. Un tel &quot;sprite&quot; a tous les états visuels pour l’élément donné positionnés l’un après l’autre. Lors du style d’un élément d’interface utilisateur avec des sprites, la même image de sprite est référencée pour tous les états différents du CSS. En outre, la propriété `background-position` est utilisée pour chaque état pour spécifier la partie de l’image &quot;sprite&quot; utilisée. Vous pouvez structurer une image &quot;sprite&quot; de n’importe quelle manière appropriée. Les visionneuses sont normalement empilées verticalement. Vous trouverez ci-dessous un exemple de style basé sur une &quot;sprite&quot; du même bouton de zoom avant :

```
.s7ecatalogsearchviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
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

Voici la documentation de référence sur les éléments de l’interface utilisateur qui s’applique à la visionneuse de recherche de catalogue électronique :

* [Bouton Ajouter un favori](r-html5-ecatsearch-customize-addfavorite.md)
* [Bouton Fermer](r-html5-ecatsearch-customize-closebutton.md)
* [Téléchargement](r-html5-ecatsearch-customize-download.md)
* [Partage des emails](r-html5-ecatsearch-customize-emailshare.md)
* [Incorporer le partage](r-html5-ecatsearch-customize-embedshare.md)
* [Partage facebook](r-html5-ecatsearch-customize-facebookshare.md)
* [Effet Favoris](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Menu Favoris](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Vue Favoris](r-html5-ecatsearch-customize-favoritesview.md)
* [Bouton Première page](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Mise en évidence de la cible](r-html5-ecatsearch-customize-focushighlight.md)
* [Bouton Plein écran](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Effet Icône](r-html5-ecatsearch-customize-iconeffect.md)
* [Fenêtre contextuelle du panneau Infos](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Effet de zone cliquable](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Bouton Grande page suivante](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Bouton Grande page précédente](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Bouton Dernière page](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Partage de liens](r-html5-ecatsearch-customize-linkshare.md)
* [Barre de contrôle principale](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Zone de visionneuse principale](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Bouton Page suivante](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Indicateur de page](r-html5-ecatsearch-customize-pageindicator.md)
* [Page vue](r-html5-ecatsearch-customize-pageview.md)
* [Bouton Page précédente](r-html5-ecatsearch-customize-previouspagebutton.md)
* [Imprimer](r-html5-ecatsearch-customize-print.md)
* [Bouton Supprimer les favoris](r-html5-ecatsearch-customize-removefavorite.md)
* [Bouton Rechercher](r-html5-ecatsearch-customize-searchbutton.md)
* [Effet de recherche](r-html5-ecatsearch-customize-searcheffect.md)
* [Panneau des résultats de recherche](r-html5-ecatsearch-customize-searchresultspanel.md)
* [Barre de contrôle Secondaire](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [Partage sur les réseaux sociaux](r-html5-ecatsearch-customize-socialshare.md)
* [Table des matières](r-html5-ecatsearch-customize-tableofcontents.md)
* [Miniatures](r-html5-ecatsearch-customize-thumbnails.md)
* [Bouton Miniatures](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [Infobulles](r-html5-ecatsearch-customize-tooltips.md)
* [Partage twitter](r-html5-ecatsearch-customize-twittershare.md)
* [Bouton Afficher tous les favoris](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Bouton Zoom avant](r-html5-ecatsearch-customize-zoominbutton.md)
* [Bouton Zoom arrière](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Bouton Réinitialiser le zoom](r-html5-ecatsearch-customize-zoomresetbutton.md)
