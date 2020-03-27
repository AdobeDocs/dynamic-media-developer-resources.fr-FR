---
description: 'null'
seo-description: 'null'
seo-title: Prise en charge du suivi d’Adobe Analytics
solution: Experience Manager
title: Prise en charge du suivi d’Adobe Analytics
topic: Dynamic media
uuid: a7de5549-2a9d-4153-be5e-72705ced85ac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge du suivi d’Adobe Analytics{#support-for-adobe-analytics-tracking}

## Suivi personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Par défaut, le lecteur envoie une requête HTTP de suivi unique au serveur d’images configuré avec le type de lecteur et les informations de version.

Pour l’intégrer aux systèmes d’analyse tiers, il est nécessaire d’écouter le rappel du `trackEvent` lecteur et de traiter l’ `eventInfo` argument de la fonction de rappel si nécessaire. Le code suivant est un exemple de cette fonction de gestionnaire :

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
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

Le lecteur effectue le suivi du utilisateur du SDK suivant :

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>utilisateur SDK  </p> </th> 
   <th colname="col2" class="entry"> <p>Envoyé quand... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CHARGEMENT </span> </p> </td> 
   <td colname="col2"> <p>le lecteur est d’abord chargé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> BANNIÈRE </span> </p> </td> 
   <td colname="col2"> <p>l’image de bannière du carrousel est modifiée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>l’utilisateur active la zone réactive. </p> </td> 
  </tr> 
 </tbody> 
</table>

