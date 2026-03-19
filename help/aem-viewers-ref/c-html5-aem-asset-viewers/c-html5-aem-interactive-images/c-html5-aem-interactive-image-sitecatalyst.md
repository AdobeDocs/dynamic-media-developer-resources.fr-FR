---
title: Prise en charge du suivi Analytics
description: Prise en charge du suivi Analytics
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 17e8937f-e328-46a4-b7d9-1fd39ab2e8bd
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# Prise en charge du suivi Analytics{#support-for-analytics-tracking}

## Tracking personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Par défaut, la visionneuse envoie une requête HTTP de suivi unique au serveur d’images configuré avec les informations de type et de version de la visionneuse.

Pour l’intégration aux systèmes d’analyse tiers, il est nécessaire d’écouter le rappel de la visionneuse `trackEvent` et de traiter l’argument `eventInfo` de la fonction de rappel si nécessaire. Le code suivant est un exemple d’une telle fonction de gestionnaire :

```javascript {.line-numbers}
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
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
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>l’utilisateur active la zone réactive. </p> </td> 
  </tr> 
 </tbody> 
</table>
