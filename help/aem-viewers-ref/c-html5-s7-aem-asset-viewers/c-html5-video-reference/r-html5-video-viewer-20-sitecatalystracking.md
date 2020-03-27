---
description: La visionneuse vidéo prend en charge le suivi prêt à l’emploi dans Adobe Analytics.
seo-description: La visionneuse vidéo prend en charge le suivi prêt à l’emploi dans Adobe Analytics.
seo-title: Prise en charge du suivi d’Adobe Analytics
solution: Experience Manager
title: Prise en charge du suivi d’Adobe Analytics
topic: Dynamic media
uuid: c53b3d3b-42e5-4c87-8a1e-87c73eb32341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge du suivi d’Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse vidéo prend en charge le suivi prêt à l’emploi dans Adobe Analytics.

## Suivi prêt à l’emploi {#section-3b101fe30be943c1b679fd5c273569ca}

La visionneuse vidéo prend en charge le suivi prêt à l’emploi dans Adobe Analytics.

Pour activer le suivi, transmettez le nom de  prédéfini approprié comme `config2` paramètre.

Le lecteur envoie également une requête HTTP de suivi unique au serveur d’images configuré avec le type de lecteur et les informations de version.

## Suivi personnalisé {#section-ab10bd7caf184721a366cf3953071934}

Pour intégrer des systèmes d’analyse tiers, il est nécessaire d’écouter le rappel du `trackEvent` lecteur et l’argument `eventInfo` de traitement de la fonction de rappel, le cas échéant. Le code suivant est un exemple de cette fonction de gestionnaire :

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
   <td colname="col2"> <p>est chargé en premier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PERMUTATION </span> </p> </td> 
   <td colname="col2"> <p>une ressource est permutée dans le lecteur à l’aide de l’ <span class="codeph"> API setAsset() </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LECTURE </span> </p> </td> 
   <td colname="col2"> <p>la lecture commence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>la lecture est interrompue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ARRET </span> </p> </td> 
   <td colname="col2"> <p>la lecture est arrêtée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JALON </span> </p> </td> 
   <td colname="col2"> <p>La lecture atteint l’une des meules suivantes : 0 %, 25 %, 50 %, 75 % et 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>

