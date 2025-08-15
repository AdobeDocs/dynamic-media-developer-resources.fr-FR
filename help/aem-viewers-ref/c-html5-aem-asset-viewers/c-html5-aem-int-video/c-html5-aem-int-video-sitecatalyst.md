---
title: Prise en charge du suivi Adobe Analytics
description: La visionneuse HTML5 Video360 prend en charge le suivi Adobe Analytics prêt à l’emploi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User,Data Engineer,Data Architect
exl-id: 74a69d01-fa58-4d36-8598-992baf6ae11d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse HTML5 Video360 prend en charge le suivi Adobe Analytics prêt à l’emploi.

Pour activer le suivi, transmettez le nom du paramètre prédéfini de société approprié en tant que paramètre `config2`.

Par défaut, la visionneuse envoie une requête HTTP de suivi unique au serveur d’images configuré avec les informations de type et de version de la visionneuse.

## Tracking personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour l’intégration aux systèmes d’analyse tiers, il est nécessaire d’écouter le rappel de la visionneuse `trackEvent` et de traiter l’argument `eventInfo` de la fonction de rappel si nécessaire. Le code suivant est un exemple d’une telle fonction de gestionnaire :

```javascript {.line-numbers}
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
 </tbody> 
</table>
