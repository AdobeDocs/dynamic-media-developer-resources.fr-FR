---
title: getComponent
description: JavaScript référence de l’API pour Carousel Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 088d99d0-600d-4e47-85ea-a9769938b88b
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# getComponent {#getcomponent}

JavaScript référence de l’API pour Carousel Viewer.

`getComponent(componentId)`

Renvoie une référence au composant SDK de la visionneuse utilisé par la visionneuse. La page Web peut utiliser cette méthode pour étendre ou personnaliser le comportement de la visionneuse prête à l’emploi. Appelez cette méthode uniquement après l’exécution du rappel de la `initComplete` visionneuse, sinon le composant ne peut pas encore être créé par la logique de visionneuse.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` : `{String}` ID du composant SDK de la visionneuse utilisé par la visionneuse. Cette visionneuse prend en charge les ID de composant suivants :

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID de composant </p> </th> 
   <th colname="col2" class="entry"> <p>Nom de la classe du composant SDK de la visionneuse </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk. ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> conteneur </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Visionneuse de supports </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Vue du carrousel </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.CarouselView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Effet d’image interactive </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Barre de contrôle </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Indicateur défini </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.SetIndicator </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Bouton suivant </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Bouton précédent </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Lorsque vous utilisez des API SDK, il est important d’utiliser l’espace de noms SDK complet correct, comme décrit dans [Espace de noms SDK de visionneuse](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-namespace.md).

Reportez-vous à la documentation de l’API du SDK de la visionneuse pour plus d’informations sur un composant particulier.

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence au composant SDK de la visionneuse. La méthode renvoie `null` si la propriété n’est `componentId` pas un composant de visionneuse pris en charge ou si le composant n’a pas encore été créé par la logique de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
} 
})
```
