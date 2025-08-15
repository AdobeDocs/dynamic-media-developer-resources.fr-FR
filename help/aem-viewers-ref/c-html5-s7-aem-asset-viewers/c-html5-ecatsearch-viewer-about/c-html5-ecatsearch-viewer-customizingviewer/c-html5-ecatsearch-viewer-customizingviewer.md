---
title: Personnalisation de la visionneuse de catalogue électronique Search
description: Toute la personnalisation visuelle et la plupart des personnalisations de comportement pour la visionneuse Search catalogue électronique s’effectuent en créant un CSS personnalisé.
keywords: sensible
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---

# Personnalisation de la visionneuse de catalogue électronique Search{#customizing-ecatalog-search-viewer}

Toute la personnalisation visuelle et la plupart des personnalisations de comportement pour la visionneuse Search catalogue électronique s’effectuent en créant un CSS personnalisé.

Le flux de travail suggéré consiste à prendre le fichier CSS par défaut pour la visionneuse appropriée, à le copier dans un emplacement différent, à le personnaliser et à spécifier l’emplacement du fichier personnalisé dans la `style=` commande.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que le fichier par défaut. Si une déclaration de classe est omise, la visionneuse ne fonctionne pas correctement car elle ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre façon de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement sur la page Web ou dans l’une des règles CSS externes liées.

Lors de la création d’une feuille CSS personnalisée, n’oubliez pas que la visionneuse attribue une `.s7ecatalogsearchviewer` classe à son élément DOM conteneur. Si vous utilisez un fichier CSS externe transmis avec la commande, utilisez `style=` la classe comme classe parent dans le `.s7ecatalogsearchviewer` sélecteur descendant de vos règles CSS. Si vous utilisez des styles incorporés sur la page Web, vous devez également qualifier ce sélecteur avec un ID de l’élément DOM conteneur comme suit :

`#<containerId>.s7ecatalogsearchviewer`

## Création d’une feuille CSS responsive conçue {#section-c1e74f5114ad418884ca1c95f5ea5b63}

Il est possible de cibler différents appareils et tailles d’intégration dans CSS pour que votre contenu s’affiche différemment, en fonction de l’appareil d’un utilisateur ou d’une mise en page Web particulière. Ce ciblage inclut, mais sans s’y limiter, différentes mises en page Web, tailles d’éléments d’interface utilisateur et résolution d’illustration.

La visionneuse prend en charge deux méthodes pour créer des CSS conçus en responsive design : les marqueurs CSS et les requêtes multimédias CSS standard. Vous pouvez utiliser ces méthodes indépendamment ou ensemble.

**Marqueurs CSS**

Pour créer un fichier CSS conçu en responsive design, la visionneuse prend en charge les marqueurs CSS que des classes CSS spéciales ont attribuées dynamiquement à l’élément conteneur de visionneuse de niveau supérieur en fonction de la taille de la visionneuse d’exécution et du type d’entrée sur le périphérique actuel.

Le premier groupe de marqueurs CSS comprend `.s7size_large`, `.s7size_medium`et `.s7size_small` les classes. Ils sont appliqués en fonction de la zone d’exécution du conteneur de la visionneuse. Autrement dit, si la zone de visualisation est égale ou supérieure à la taille d’un moniteur `.s7size_large` de bureau commun est utilisée, si la zone est proche de la taille d’une tablette `.s7size_medium` commune est attribuée. Pour des zones similaires à celles des écrans de téléphone portable. Le marqueur `.s7size_small` est défini. L’objectif principal de ces marqueurs CSS est de créer différentes dispositions d’interface utilisateur pour différents écrans et tailles de visionneuses.

Le deuxième groupe de marqueurs CSS comprend `.s7mouseinput` et `.s7touchinput`. Le marqueur `.s7touchinput` est défini si le périphérique actuel dispose de capacités d’entrée tactile ; sinon, `.s7mouseinput` est utilisé. Ces marqueurs sont destinés à créer des éléments d’entrée d’interface utilisateur avec différentes tailles d’écran pour différents types d’entrée, car normalement l’entrée tactile nécessite des éléments plus grands. Dans le cas où l’appareil dispose à la fois de capacités d’entrée de souris et tactiles, `.s7touchinput` est défini et le spectateur rend une interface utilisateur tactile.

L’exemple de CSS suivant définit la taille du bouton de zoom avant sur 28 x 28 pixels sur les systèmes avec entrée souris et 56 x 56 pixels sur les périphériques tactiles. De plus, le bouton est complètement masqué si la taille de la visionneuse devient trop petite :

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

Pour cibler des périphériques avec une densité de pixels différente, utilisez des requêtes de média CSS. Le bloc de requête de média suivant contiendrait un code CSS spécifique aux écrans haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation de marqueurs CSS est le moyen le plus flexible de créer des CSS conçus en responsive design. Il vous permet de cibler non seulement la taille de l’écran de l’appareil, mais aussi la taille réelle de la visionneuse, ce qui est utile pour les mises en page conçues en responsive design.

Utilisez le fichier CSS de la visionneuse par défaut comme exemple d’approche de marqueurs CSS.

**Requêtes de média CSS**

La détection des périphériques peut également être effectuée à l’aide de requêtes de média CSS pures. Tout ce qui est inclus dans un bloc de requête de média donné n’est appliqué que lorsqu’il est exécuté sur un périphérique correspondant.

Lorsqu’elles sont appliquées aux visionneuses mobiles, utilisez quatre requêtes de média CSS, définies dans votre fichier CSS dans l’ordre suivant :

1. Contient uniquement des règles spécifiques à tous les appareils tactiles.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

## CSS Sprites {#section-9d570f95eb2443aca74c1b02f6e89aff}

De nombreux éléments de l’interface utilisateur de la visionneuse sont stylisés à l’aide d’illustrations bitmap et ont plusieurs états visuels distincts. Un bon exemple est un bouton qui a normalement au moins trois états différents : « haut », « au-dessus » et « bas ». Chaque état requiert l’affectation d’une illustration bitmap.

Avec une approche classique du style, le CSS aurait une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de CSS permettant d’appliquer un style à un bouton de zoom avant :

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

L’inconvénient de cette approche est que l’utilisateur final rencontre une réponse scintillante ou retardée de l’interface utilisateur lorsque l’élément est interagi avec pour la première fois. Cette action se produit car l’illustration d’image pour le nouvel état d’élément n’est pas encore téléchargée. En outre, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

CSS sprites est une approche différente où l’illustration d’image pour tous les états d’élément est combinée dans un seul fichier PNG appelé « sprite ». Un tel « sprite » a tous les états visuels de l’élément donné positionnés les uns après les autres. Lors du style d’un élément d’interface utilisateur avec des sprites, la même image de sprite est référencée pour tous les différents états dans le CSS. En outre, la `background-position` propriété est utilisée pour chaque état afin de spécifier quelle partie de l’image « sprite » est utilisée. Vous pouvez structurer une image « sprite » de n’importe quelle manière appropriée. Les téléspectateurs l’ont normalement empilé verticalement. Voici un exemple basé sur « sprite » d’un style du même bouton de zoom avant ci-dessus :

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

## Notes générales de style et conseils {#section-95855dccbbc444e79970f1aaa3260b7b}

* Lors de la personnalisation de l’interface utilisateur de la visionneuse avec CSS, l’utilisation de la règle n’est pas prise en charge pour mettre en `!IMPORTANT` forme les éléments de la visionneuse. En particulier, `!IMPORTANT` la règle ne doit pas être utilisée pour remplacer un style par défaut ou d’exécution fourni par la visionneuse ou le Kit de développement logiciel (SDK) de la visionneuse. La raison en est que cela peut affecter le comportement des composants appropriés. Au lieu de cela, vous devez utiliser des sélecteurs CSS avec la spécificité appropriée pour définir les propriétés CSS qui sont documentées dans ce guide de référence.
* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS, et non à l’emplacement de la page HTML de la visionneuse. Tenez compte de cette règle lorsque vous copiez le fichier CSS par défaut vers un autre emplacement. Copiez également les ressources par défaut ou mettez à jour les chemins d’accès dans la feuille CSS personnalisée.
* Le format préféré pour les illustrations bitmap est PNG.
* L’illustration bitmap est affectée aux éléments de l’interface utilisateur à l’aide de la `background-image` propriété.
* Les `width` propriétés et `height` d’un élément d’interface utilisateur définissent sa taille logique. La taille du bitmap transmis à `background-image` n’affecte pas la taille logique.
* Pour utiliser la densité de pixels élevée des écrans haute résolution tels que Retina, spécifiez une illustration bitmap deux fois plus grande que la taille de l’élément de l’interface utilisateur logique. Ensuite, appliquez la `-webkit-background-size:contain` propriété pour réduire l’arrière-plan à la taille de l’élément de l’interface utilisateur logique.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` un bouton à sa classe CSS.
* Vous pouvez utiliser différents formats de valeurs colorimétriques pris en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

## Éléments courants de l’interface utilisateur {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici la documentation de référence des éléments d’interface utilisateur qui s’applique à la visionneuse de Search de catalogue électronique :

* [Bouton Ajouter un favori](r-html5-ecatsearch-customize-addfavorite.md)
* [Bouton Fermer](r-html5-ecatsearch-customize-closebutton.md)
* [Téléchargement](r-html5-ecatsearch-customize-download.md)
* [Partage email](r-html5-ecatsearch-customize-emailshare.md)
* [Partager intégré](r-html5-ecatsearch-customize-embedshare.md)
* [Partage Facebook](r-html5-ecatsearch-customize-facebookshare.md)
* [Effet Favoris](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Menu Favoris](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Vue Favoris](r-html5-ecatsearch-customize-favoritesview.md)
* [Bouton Première page](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Mise au point](r-html5-ecatsearch-customize-focushighlight.md)
* [Bouton Plein écran](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Effet d’icône](r-html5-ecatsearch-customize-iconeffect.md)
* [Fenêtre contextuelle du panneau d’informations](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Effet d’image interactive](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Grand bouton Page suivante](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Grand bouton de page précédente](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Bouton Dernière page](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Partager le lien](r-html5-ecatsearch-customize-linkshare.md)
* [Barre de contrôle principale](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Zone principale de la visionneuse](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Bouton Page suivante](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Indicateur de page](r-html5-ecatsearch-customize-pageindicator.md)
* [Page vue](r-html5-ecatsearch-customize-pageview.md)
* [Bouton Page précédente](r-html5-ecatsearch-customize-previouspagebutton.md)
* [Imprimer](r-html5-ecatsearch-customize-print.md)
* [Bouton Supprimer les favoris](r-html5-ecatsearch-customize-removefavorite.md)
* [Bouton Search](r-html5-ecatsearch-customize-searchbutton.md)
* [Search effet](r-html5-ecatsearch-customize-searcheffect.md)
* [Search panneau Résultats](r-html5-ecatsearch-customize-searchresultspanel.md)
* [Barre de contrôle secondaire](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [Social partager](r-html5-ecatsearch-customize-socialshare.md)
* [Table des matières](r-html5-ecatsearch-customize-tableofcontents.md)
* [Vignettes](r-html5-ecatsearch-customize-thumbnails.md)
* [Bouton Miniatures](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [Info-bulles](r-html5-ecatsearch-customize-tooltips.md)
* [Partage Twitter](r-html5-ecatsearch-customize-twittershare.md)
* [Bouton Afficher tous les favoris](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Bouton Zoom avant](r-html5-ecatsearch-customize-zoominbutton.md)
* [Bouton Zoom arrière](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Bouton de réinitialisation du zoom](r-html5-ecatsearch-customize-zoomresetbutton.md)
