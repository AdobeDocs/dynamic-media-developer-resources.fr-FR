---
description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique
seo-description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: 4e5b79b5-4a2b-427a-b527-81247a6b740d
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# getComponent{#getcomponent}

Référence de l’API JavaScript pour la visionneuse de catalogue électronique

[!DNL `getComponent(componentId)`]

Renvoie une référence au composant SDK de la visionneuse utilisé par la visionneuse. La page Web peut utiliser cette méthode pour étendre ou personnaliser le comportement du lecteur prêt à l’emploi. Appelez cette méthode uniquement après l’exécution du rappel de la `initComplete` visionneuse, sans quoi le composant ne sera pas encore créé par la logique de la visionneuse.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`componentID`*` : `{String}` identifiant du composant SDK du lecteur de contenu utilisé par le lecteur de contenu. Cette visionneuse prend en charge les ID de composant suivants :

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID de composant </p> </th> 
   <th colname="col2" class="entry"> <p>Nom de classe du composant SDK de visionneuse </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> conteneur </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common. </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pageView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.PageView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PrimaryControls </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryControls </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gridView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.ThumbnailGridView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tableOfContents </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.TableOfContents </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> infoPanelPopup </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.info.InfoPanelPopup </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ImageMapEffect </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> leftButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rightButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomInButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomOutButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryZoomResetButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> thumbnailPageButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ThumbnailPageButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toolBarLeftButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toolBarRightButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> firstPageButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryFirstPageButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> lastPageButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryLastPageButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> socialShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> twitterShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> facebookShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linkShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> emailShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.EmailShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> embedShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.EmbedShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imprimer </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.Print </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> télécharger </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Download </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> favoritesEffect </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.FavorisEffect </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> favorisView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.FavorisView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> favoritesMenu </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.FavorisMenu </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> addFavoriteButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.AddFavoriteButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> removeFavoriteButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.RemoveFavoriteButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> viewAllFavoriteButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.ViewAllFavoriteButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> searchButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.SearchButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> searchPanel </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.search.SearchPanel </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> searchManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.search.SearchManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> searchEffect </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.search.SearchEffect </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Lorsque vous travaillez avec des API SDK, il est important d’utiliser le SDK complet  correctement qualifié, comme décrit dans le SDK du [lecteur de contenu,  le](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-html5-viewer-sdk-namespace.md#concept-16ce67bfbdc64ffc8fc7ad174f208f05)de  de SDK.

Pour plus d’informations sur un composant spécifique, consultez la documentation de l’API *du SDK* du lecteur.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` une référence au composant SDK de visionneuse. La méthode renvoie `null` si le `componentId` composant n’est pas un composant de visionneuse pris en charge ou si le composant n’a pas encore été créé par la logique de la visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
} 
})
```

