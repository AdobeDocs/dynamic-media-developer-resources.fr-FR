---
title: getComponent
description: Référence de l’API JavaScript pour la visionneuse d’images vidéo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 5f2514a9-bbd0-436d-ad96-b89778604f8a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# getComponent{#getcomponent}

Référence de l’API JavaScript pour la visionneuse d’images vidéo.

`getComponent(componentId)`

Renvoie une référence au composant SDK de la visionneuse utilisé par la visionneuse. La page web peut utiliser cette méthode pour étendre ou personnaliser le comportement de la visionneuse prête à l’emploi. Appelez cette méthode uniquement après l’exécution du rappel de la visionneuse `initComplete`, sinon le composant ne peut pas encore être créé par la logique de la visionneuse.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` : identifiant du composant SDK de la visionneuse utilisé par la visionneuse. Cette visionneuse prend en charge les identifiants de composant suivants :

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Identifiant du composant </p> </th> 
   <th colname="col2" class="entry"> <p>Nom de classe du composant SDK de visionneuse </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Lorsque vous utilisez des API SDK, il est important d’utiliser l’espace de noms du SDK complet correct, comme décrit dans la section [Espace de noms du SDK de la visionneuse](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-namespace.md#concept-00a31b9bc7eb4014b28c1ba661fe5265).

Pour plus d’informations sur un composant particulier, consultez la documentation de l’API du SDK de la visionneuse .

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence au composant SDK de visionneuse. La méthode renvoie `null` si le `componentId` n’est pas un composant de visionneuse pris en charge ou si le composant n’a pas encore été créé par la logique de la visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```
