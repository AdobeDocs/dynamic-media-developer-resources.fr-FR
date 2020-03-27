---
description: La visionneuse de vidéos HTML5 Video360 prend en charge le suivi prêt à l’emploi d’Adobe Analytics.
seo-description: La visionneuse de vidéos HTML5 Video360 prend en charge le suivi prêt à l’emploi d’Adobe Analytics.
seo-title: Prise en charge du suivi d’Adobe Analytics
solution: Experience Manager
title: Prise en charge du suivi d’Adobe Analytics
topic: Dynamic media
uuid: b5ab903b-3365-45e3-9542-c290c6c42670
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge du suivi d’Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse de vidéos HTML5 Video360 prend en charge le suivi prêt à l’emploi d’Adobe Analytics.

Pour activer le suivi, transmettez le nom de  prédéfini approprié comme `config2` paramètre.

Par défaut, le lecteur envoie une requête HTTP de suivi unique au serveur d’images configuré avec le type de lecteur et les informations de version.

## Suivi personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour intégrer des systèmes d’analyse tiers, il est nécessaire d’écouter le rappel de la `trackEvent` visionneuse et de traiter l’ `eventInfo` argument de la fonction de rappel si nécessaire. Le code suivant est un exemple de cette fonction de gestionnaire :

```
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

Le lecteur effectue le suivi du utilisateur du SDK suivant :

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>utilisateur SDK  </p> </th> 
   <th colname="col2" class="entry"> <p>Envoyé... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CHARGEMENT </span> </p> </td> 
   <td colname="col2"> <p>lorsque le lecteur est chargé en premier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PERMUTATION </span> </p> </td> 
   <td colname="col2"> <p>lorsqu’un fichier est interverti dans le lecteur à l’aide de l’ <span class="codeph"> API setAsset() </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LECTURE </span> </p> </td> 
   <td colname="col2"> <p>lors de la  de lecture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>en cas d’interruption de la lecture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ARRET </span> </p> </td> 
   <td colname="col2"> <p>lorsque la lecture est arrêtée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JALON </span> </p> </td> 
   <td colname="col2"> <p>lorsque la lecture atteint l’un des jalons suivants : 0 %, 25 %, 50 %, 75 % ou 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>

