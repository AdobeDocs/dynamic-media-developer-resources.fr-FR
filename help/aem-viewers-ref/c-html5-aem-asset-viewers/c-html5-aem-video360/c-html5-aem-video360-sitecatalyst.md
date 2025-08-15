---
title: Prise en charge du suivi Adobe Analytics
description: Prise en charge du suivi Adobe Analytics
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

Par défaut, la visionneuse envoie une seule requête HTTP de suivi au serveur d’images configuré avec le type et les informations de version de la visionneuse.

## Suivi personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour intégrer des systèmes d’analyse tiers, il est nécessaire d’écouter le rappel de la `trackEvent` visionneuse et de traiter l’argument `eventInfo` de la fonction de rappel si nécessaire. Le code suivant est un exemple de fonction de gestionnaire :

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
   <th colname="col1" class="entry"> <p>Evénement utilisateur SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Envoyèrent... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CHARGER </span> </p> </td> 
   <td colname="col2"> <p>Lorsque la visionneuse est chargée en premier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ÉCHANGER </span> </p> </td> 
   <td colname="col2"> <p>lorsqu’une ressource est permutée dans la visionneuse à l’aide <span class="codeph"> de l’API setAsset(). </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JOUER </span> </p> </td> 
   <td colname="col2"> <p>au démarrage de la lecture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>lorsque la lecture est interrompue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ARRÊTER </span> </p> </td> 
   <td colname="col2"> <p>lorsque la lecture est arrêtée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JALON </span> </p> </td> 
   <td colname="col2"> <p>lorsque la lecture atteint l’un des jalons suivants : 0 %, 25 %, 50 %, 75 % ou 100 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> INTERACTIVE_SWATCH </span> </p> </td> 
   <td colname="col2"> <p>Chaque fois que l’utilisateur clique sur un échantillon interactif. </p> </td> 
  </tr> 
 </tbody> 
</table>
