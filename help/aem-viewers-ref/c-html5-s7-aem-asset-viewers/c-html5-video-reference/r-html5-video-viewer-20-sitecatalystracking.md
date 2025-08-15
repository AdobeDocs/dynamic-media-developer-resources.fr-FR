---
title: Prise en charge du suivi Adobe Analytics
description: La visionneuse vidéo prend en charge le suivi Adobe Analytics prêt-à-l’emploi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 2cc7087d-ed02-4560-b9ce-533af2b11a24
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse vidéo prend en charge le suivi Adobe Analytics prêt-à-l’emploi.

## Tracking d’usine {#section-3b101fe30be943c1b679fd5c273569ca}

La visionneuse vidéo prend en charge le suivi Adobe Analytics prêt-à-l’emploi.

Pour activer le suivi, transmettez le nom du paramètre prédéfini de la société en tant que `config2` paramètre.

La visionneuse envoie également une requête HTTP de suivi unique au serveur d’images configuré avec le type et les informations de version de la visionneuse.

## Suivi personnalisé {#section-ab10bd7caf184721a366cf3953071934}

Pour intégrer des systèmes d’analyse tiers, il est nécessaire d’écouter le `trackEvent` rappel de la visionneuse et de traiter `eventInfo` l’argument de la fonction de rappel si nécessaire. Le code suivant est un exemple de fonction de gestionnaire :

```javascript {.line-numbers}
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

La visionneuse effectue le suivi des événements utilisateur SDK suivants :

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Evénement utilisateur SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Envoyé quand... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CHARGER </span> </p> </td> 
   <td colname="col2"> <p>La visionneuse est chargée en premier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ÉCHANGER </span> </p> </td> 
   <td colname="col2"> <p>une ressource est permutée dans la visionneuse à l’aide <span class="codeph"> de l’API setAsset(). </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JOUER </span> </p> </td> 
   <td colname="col2"> <p>La lecture démarre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>La lecture est interrompue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ARRÊTER </span> </p> </td> 
   <td colname="col2"> <p>La lecture est arrêtée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JALON </span> </p> </td> 
   <td colname="col2"> <p>La lecture atteint l’une des meules suivantes : 0 %, 25 %, 50 %, 75 % et 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>
