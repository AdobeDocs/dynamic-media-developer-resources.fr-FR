---
description: Référence de l’API JavaScript pour la visionneuse de carrousel.
seo-description: Référence de l’API JavaScript pour la visionneuse de carrousel.
seo-title: getComponent**
solution: Experience Manager
title: getComponent**
topic: Dynamic media
uuid: b5449564-c01c-4bb3-b265-b8d70e5f1b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getComponent**{#getcomponent}

Référence de l’API JavaScript pour la visionneuse de carrousel.

`getComponent(componentId)`

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
   <td colname="col1"> <p> <span class="codeph"> carouselView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.CarouselView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> controlBar </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> setIndicator </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.SetIndicator </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nextButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> prevButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Lorsque vous travaillez avec des API SDK, il est important d’utiliser le de SDK  qualifié approprié, comme décrit dans le kit SDK de [lecteur de contenu,  le](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-namespace.md)SDK.

Pour plus d’informations sur un composant particulier, consultez la documentation de l’API du SDK de lecteur.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` une référence au composant SDK de visionneuse. La méthode renvoie `null` si le `componentId` composant n’est pas un composant de visionneuse pris en charge ou si le composant n’a pas encore été créé par la logique de la visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
} 
})
```

