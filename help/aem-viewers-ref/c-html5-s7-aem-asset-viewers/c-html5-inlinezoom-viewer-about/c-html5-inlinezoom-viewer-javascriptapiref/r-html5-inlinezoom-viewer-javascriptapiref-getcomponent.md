---
title: getComponent
description: Référence de l’API JavaScript pour la visionneuse de zoom intégré
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 72ae83e4-b879-4b3b-a5d9-38ed0fc2969d
TQID: 'https://experienceleague.adobe.com/xQrZhZSL6qi1p6FqxSMiP0gxtIMxpFziEh5EvE0AO8s'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 1%

---

# getComponent{#getcomponent}

Référence de l’API JavaScript pour la visionneuse de zoom intégré

`getComponent(componentId)`

Renvoie une référence au composant SDK de la visionneuse utilisé par la visionneuse. La page web peut utiliser cette méthode pour étendre ou personnaliser le comportement de la visionneuse prête à l’emploi. Appelez cette méthode uniquement après l’exécution du rappel de la visionneuse `initComplete`. Dans le cas contraire, le composant ne sera peut-être pas encore créé par la logique de la visionneuse.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` l’identifiant du composant SDK de la visionneuse utilisé par la visionneuse. Cette visionneuse prend en charge les identifiants de composant suivants :

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID de composant </p> </th> 
   <th colname="col2" class="entry"> <p>Nom de classe du composant SDK de la visionneuse </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de conteneur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> déroulante <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.FlyoutZoomView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> d’échantillons </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Lorsque vous utilisez des API SDK, il est important d’utiliser correctement l’espace de noms SDK complet, comme décrit dans la section [SDK de la visionneuse](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-namespace.md#concept-5af3b472b320496d87735ea612edda80).

Reportez-vous à la documentation du SDK de visionneuse pour plus d’informations sur un composant particulier.

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence au composant SDK de la visionneuse. La méthode renvoie la valeur `null` si le `componentId` n’est pas un composant de visionneuse pris en charge ou si le composant n’a pas encore été créé par la logique de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyoutZoomView = <instance>.getComponent("flyout"); 
} 
})
```
