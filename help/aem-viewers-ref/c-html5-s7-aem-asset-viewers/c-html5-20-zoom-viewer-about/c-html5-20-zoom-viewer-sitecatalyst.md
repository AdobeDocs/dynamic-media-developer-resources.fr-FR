---
title: Prise en charge du suivi Adobe Analytics
description: Prise en charge du suivi Adobe Analytics
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 5f927a4b-b9c8-4750-9d1c-c252d87fd236
TQID: 'https://experienceleague.adobe.com/4XIzFFsX43NZBy4uB5WRZeIs92EWpbT8U2BsnTsmlDU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 0%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

## Tracking d’usine {#section-ba994f079d0343c8ae48adffaa3195a3}

La visionneuse de vidéos prend en charge le suivi [!DNL Adobe Analytics] prêt à l’emploi. Pour activer le suivi, transmettez le nom du paramètre prédéfini de société approprié en tant que paramètre `config2`.

La visionneuse envoie également une requête HTTP de suivi unique au serveur d’images configuré avec les informations de type et de version de la visionneuse.

## Tracking personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour l’intégration aux systèmes d’analyse tiers, il est nécessaire d’écouter le rappel de la visionneuse `trackEvent` et de traiter l’argument `eventInfo` de la fonction de rappel si nécessaire. Le code suivant est un exemple d’une telle fonction de gestionnaire :

```javascript {.line-numbers}
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
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
   <td colname="col1"> <p> </span> DE CHARGEMENT <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>La visionneuse est chargée en premier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>une ressource est permutée dans la visionneuse à l’aide de l’API </span> setAsset() <span class="codeph">. </p> </td> 
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
   <td colname="col1"> <p> </span> D’ÉCHANTILLON <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> une image est modifiée en cliquant ou en appuyant sur un échantillon. </p> </td> 
  </tr> 
 </tbody> 
</table>

