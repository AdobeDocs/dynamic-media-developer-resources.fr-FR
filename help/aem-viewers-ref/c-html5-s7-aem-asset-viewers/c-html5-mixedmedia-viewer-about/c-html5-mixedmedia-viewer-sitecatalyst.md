---
title: Prise en charge du suivi Adobe Analytics
description: La visionneuse de médias mixtes prend en charge le suivi Adobe Analytics prêt à l’emploi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3b28c853-3747-4805-a141-3cce1398d783
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse de médias mixtes prend en charge le suivi Adobe Analytics prêt à l’emploi.

## Tracking d’usine {#section-ba994f079d0343c8ae48adffaa3195a3}

La visionneuse de médias mixtes prend en charge le suivi [!DNL Adobe Analytics] prêt à l’emploi. Pour activer le suivi, transmettez le nom du paramètre prédéfini de société approprié en tant que paramètre `config2`.

La visionneuse envoie également une requête HTTP de suivi unique au serveur d’images configuré avec les informations de type et de version de la visionneuse.

## Tracking personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour l’intégration aux systèmes d’analyse tiers, il est nécessaire d’écouter le rappel de la visionneuse `trackEvent` et de traiter l’argument `eventInfo` de la fonction de rappel si nécessaire. Le code suivant est un exemple d’une telle fonction de gestionnaire :

```javascript {.line-numbers}
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
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
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>une ressource est permutée dans la visionneuse à l’aide de <span class="codeph">’API setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>une image fait l’objet d’un zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>une image est panoramique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> D’ÉCHANTILLON </span> </p> </td> 
   <td colname="col2"> <p> une image est modifiée en cliquant ou en appuyant sur un échantillon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>la lecture est démarrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>la lecture est suspendue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>la lecture est arrêtée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JALON </span> </p> </td> 
   <td colname="col2"> <p>la lecture atteint l’une des étapes suivantes : 0 %, 25 %, 50 %, 75 % et 100 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPIN </span> </p> </td> 
   <td colname="col2"> <p>la rotation est effectuée. </p> </td> 
  </tr> 
 </tbody> 
</table>
