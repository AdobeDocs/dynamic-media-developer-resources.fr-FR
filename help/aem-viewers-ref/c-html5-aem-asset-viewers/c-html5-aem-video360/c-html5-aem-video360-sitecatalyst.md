---
title: Prise en charge du suivi Adobe Analytics
description: Prise en charge du suivi Adobe Analytics
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

Par défaut, la visionneuse envoie une requête HTTP de suivi unique au serveur d’images configuré avec les informations de type et de version de la visionneuse.

## Tracking personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour l’intégration aux systèmes d’analyse tiers, il est nécessaire d’écouter le rappel de la visionneuse `trackEvent` et de traiter l’argument `eventInfo` de la fonction de rappel si nécessaire. Le code suivant est un exemple d’une telle fonction de gestionnaire :

```javascript {.line-numbers}
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   case "INTERACTIVE_SWATCH": 
    //custom event processing code which handles user clicks on interactive swatches 
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
   <th colname="col2" class="entry"> <p>Envoyé... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DE CHARGEMENT </span> </p> </td> 
   <td colname="col2"> <p>lorsque la visionneuse est chargée en premier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>lorsqu’une ressource est permutée dans la visionneuse à l’aide de <span class="codeph">’API setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>lorsque la lecture commence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>lorsque la lecture est suspendue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>lorsque la lecture est arrêtée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JALON </span> </p> </td> 
   <td colname="col2"> <p>lorsque la lecture atteint l’un des jalons suivants : 0 %, 25 %, 50 %, 75 % ou 100 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> INTERACTIVE_SWATCH </span> </p> </td> 
   <td colname="col2"> <p>chaque fois que l’utilisateur clique sur un échantillon interactif. </p> </td> 
  </tr> 
 </tbody> 
</table>
