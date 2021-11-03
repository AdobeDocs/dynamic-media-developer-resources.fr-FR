---
description: La visionneuse vidéo avec recadrage intelligent prend en charge le suivi Adobe Analytics prêt à l’emploi.
solution: Experience Manager
title: Prise en charge du suivi Adobe Analytics
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 2cc7087d-ed02-4560-b9ce-533af2b11a24
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse vidéo avec recadrage intelligent prend en charge le suivi Adobe Analytics prêt à l’emploi.

## Suivi d’usine {#section-3b101fe30be943c1b679fd5c273569ca}

La visionneuse vidéo avec recadrage intelligent prend en charge le suivi Adobe Analytics prêt à l’emploi.

Pour activer le suivi, transmettez le nom de paramètre prédéfini d’entreprise approprié en tant que `config2` .

La visionneuse envoie également une requête HTTP de suivi unique au serveur d’images configuré avec le type de visionneuse et les informations de version.

## Suivi personnalisé {#section-ab10bd7caf184721a366cf3953071934}

Pour intégrer des systèmes d’analyse tiers, il est nécessaire d’écouter `trackEvent` rappel et processus de visionneuse `eventInfo` de la fonction de rappel, le cas échéant. Le code suivant est un exemple de fonction de gestionnaire de ce type :

```
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
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

La visionneuse effectue le suivi des événements utilisateur du SDK suivants :

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Événement d’utilisateur du SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Envoyé lorsque.. </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CHARGEMENT </span> </p> </td> 
   <td colname="col2"> <p>la visionneuse est d’abord chargée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PERMUTATION </span> </p> </td> 
   <td colname="col2"> <p>une ressource est permutée dans la visionneuse à l’aide de <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LECTURE </span> </p> </td> 
   <td colname="col2"> <p>la lecture démarre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>la lecture est suspendue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ARRET </span> </p> </td> 
   <td colname="col2"> <p>la lecture est arrêtée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JALON </span> </p> </td> 
   <td colname="col2"> <p>La lecture atteint l’une des millisecondes suivantes : 0 %, 25 %, 50 %, 75 % et 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>
