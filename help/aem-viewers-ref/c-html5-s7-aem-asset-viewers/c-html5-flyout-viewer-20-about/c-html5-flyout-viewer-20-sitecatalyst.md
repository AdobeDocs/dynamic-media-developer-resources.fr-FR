---
title: Prise en charge du suivi Adobe Analytics
description: La visionneuse déroulante prend en charge le suivi Adobe Analytics prêt à l’emploi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User,Data Engineer,Data Architect
exl-id: 6b6216f4-34dc-496f-a0c3-e97d48da14c6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 2%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse déroulante prend en charge le suivi Adobe Analytics prêt à l’emploi.

## Suivi d’usine {#section-ba994f079d0343c8ae48adffaa3195a3}

La visionneuse Fenêtre déroulante prend en charge [!DNL Adobe Analytics] suivi prêt à l’emploi. Pour activer le suivi, transmettez le nom de paramètre prédéfini d’entreprise approprié en tant que `config2` .

La visionneuse envoie également une requête HTTP de suivi unique au serveur d’images configuré avec le type de visionneuse et les informations de version.

## Suivi personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour s’intégrer à des systèmes d’analyse tiers, il est nécessaire d’écouter la `trackEvent` rappel de la visionneuse et traitement de la `eventInfo` de la fonction de rappel, le cas échéant. Le code suivant est un exemple de fonction de gestionnaire de ce type :

```javascript {.line-numbers}
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
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
   <td colname="col2"> <p>la visionneuse est chargée en premier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PERMUTATION </span> </p> </td> 
   <td colname="col2"> <p>une ressource est permutée dans la visionneuse à l’aide de <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>la fenêtre déroulante est activée ou le niveau de zoom est modifié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PANORAMIQUE </span> </p> </td> 
   <td colname="col2"> <p> une image est numérisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> NUANCES </span> </p> </td> 
   <td colname="col2"> <p> une image est modifiée en cliquant ou en appuyant sur un échantillon. </p> </td> 
  </tr> 
 </tbody> 
</table>
