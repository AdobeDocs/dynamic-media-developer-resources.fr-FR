---
description: La visionneuse de recherche de catalogue électronique prend en charge le suivi Adobe Analytics prêt à l’emploi.
solution: Experience Manager
title: Prise en charge du suivi Adobe Analytics
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User,Data Engineer,Data Architect
exl-id: b35e52f5-fa08-4945-aa52-9fdf41a6081a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse de recherche de catalogue électronique prend en charge le suivi Adobe Analytics prêt à l’emploi.

## Tracking d’usine {#section-ba994f079d0343c8ae48adffaa3195a3}

La visionneuse de recherche de catalogue électronique prend en charge le suivi [!DNL Adobe Analytics] prêt à l’emploi. Pour activer le suivi, transmettez le nom du paramètre prédéfini de société approprié en tant que paramètre `config2`.

La visionneuse envoie également une requête HTTP de suivi unique au serveur d’images configuré avec les informations de type et de version de la visionneuse.

## Tracking personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour l’intégration aux systèmes d’analyse tiers, il est nécessaire d’écouter le rappel de la visionneuse `trackEvent` et de traiter l’argument `eventInfo` de la fonction de rappel , si nécessaire. Le code suivant est un exemple d’une telle fonction de gestionnaire :

```javascript {.line-numbers}
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

La visionneuse effectue le suivi des événements utilisateur SDK suivants :

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Événement utilisateur SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Envoyé lorsque... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DE CHARGEMENT </span> </p> </td> 
   <td colname="col2"> <p>La visionneuse est chargée en premier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ÉCHANGER </span> </p> </td> 
   <td colname="col2"> <p>une ressource est permutée dans la visionneuse à l’aide de l’API <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> une image fait l’objet d’un zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>une image est panoramique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> D’ÉCHANTILLON </span> </p> </td> 
   <td colname="col2"> <p> une image est modifiée en cliquant ou en appuyant sur un échantillon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DE PAGE </span> </p> </td> 
   <td colname="col2"> <p> une image actuelle est modifiée dans la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ARTICLE </span> </p> </td> 
   <td colname="col2"> <p>Une fenêtre contextuelle Panneau d’informations est activée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>un utilisateur accède à une autre page en cliquant sur la zone cliquable. </p> </td> 
  </tr> 
 </tbody> 
</table>
