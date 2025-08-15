---
title: getComponent
description: JavaScript référence de l’API pour la visionneuse panoramique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# getComponent{#getcomponent}

JavaScript référence de l’API pour la visionneuse panoramique

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
   <td colname="col1"> <p> <span class="codeph"> vue panoramique </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.Vue panoramique </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Lorsque vous utilisez des API SDK, il est important d’utiliser un espace de noms SDK complet correct, comme décrit dans [Espace de noms SDK de visionneuse](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621).

Consultez la documentation de l’API du Kit de développement logiciel (SDK) de la visionneuse pour plus d’informations sur un composant particulier.

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` référence au composant SDK de la visionneuse. La méthode renvoie `null` si la propriété n’est `componentId` pas un composant de visionneuse pris en charge ou si le composant n’a pas encore été créé par la logique de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
} 
})
```
