---
description: La visionneuse Fenêtre déroulante prend en charge le suivi Adobe Analytics prêt à l’emploi.
seo-description: La visionneuse Fenêtre déroulante prend en charge le suivi Adobe Analytics prêt à l’emploi.
seo-title: Prise en charge du suivi Adobe Analytics
solution: Experience Manager
title: Prise en charge du suivi Adobe Analytics
uuid: 204857d3-744a-4c11-90db-1b18ff5ea5df
feature: Dynamic Media Classic, Visionneuses, SDK/API, Fenêtre déroulante
role: Développeur, Professionnel, Ingénieur de données, Architecte de données
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 2%

---


# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse Fenêtre déroulante prend en charge le suivi Adobe Analytics prêt à l’emploi.

## Suivi prêt à l’emploi {#section-ba994f079d0343c8ae48adffaa3195a3}

La visionneuse Fenêtre déroulante prend en charge [!DNL Adobe Analytics] le suivi prêt à l’emploi. Pour activer le suivi, transmettez le nom de paramètre prédéfini de société approprié sous la forme du paramètre `config2`.

La visionneuse envoie également une requête HTTP de suivi unique au serveur d’images configuré avec le type de visionneuse et les informations de version.

## Suivi personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour intégrer des systèmes d’analyse tiers, il est nécessaire d’écouter le rappel de la visionneuse `trackEvent` et de traiter l’argument `eventInfo` de la fonction de rappel si nécessaire. Le code suivant est un exemple de cette fonction de gestionnaire :

```
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

Le lecteur effectue le suivi des événements d’utilisateur SDK suivants :

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ÉVÉNEMENT utilisateur du SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Envoyé quand... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CHARGEMENT </span> </p> </td> 
   <td colname="col2"> <p>le lecteur est chargé en premier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PERMUTATION </span> </p> </td> 
   <td colname="col2"> <p>une ressource est permutée dans le lecteur à l’aide de l’API <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>la fenêtre déroulante est activée ou le niveau de zoom est modifié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PANORAMIQUE </span> </p> </td> 
   <td colname="col2"> <p> une image est panoramique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> NUANCES </span> </p> </td> 
   <td colname="col2"> <p> une image est modifiée en cliquant ou en appuyant sur une nuance. </p> </td> 
  </tr> 
 </tbody> 
</table>

