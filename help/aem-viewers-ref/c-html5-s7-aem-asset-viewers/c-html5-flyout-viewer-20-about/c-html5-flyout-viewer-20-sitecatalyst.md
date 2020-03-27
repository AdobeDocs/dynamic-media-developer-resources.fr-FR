---
description: Le lecteur de fenêtre déroulante prend en charge le suivi Adobe Analytics prêt à l’emploi.
seo-description: Le lecteur de fenêtre déroulante prend en charge le suivi Adobe Analytics prêt à l’emploi.
seo-title: Prise en charge du suivi d’Adobe Analytics
solution: Experience Manager
title: Prise en charge du suivi d’Adobe Analytics
topic: Dynamic media
uuid: 204857d3-744a-4c11-90db-1b18ff5ea5df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge du suivi d’Adobe Analytics{#support-for-adobe-analytics-tracking}

Le lecteur de fenêtre déroulante prend en charge le suivi Adobe Analytics prêt à l’emploi.

## Suivi prêt à l’emploi {#section-ba994f079d0343c8ae48adffaa3195a3}

La visionneuse Fenêtre déroulante prend en charge le [!DNL Adobe Analytics] suivi prêt à l’emploi. Pour activer le suivi, transmettez le nom de  prédéfini approprié comme `config2` paramètre.

Le lecteur envoie également une requête HTTP de suivi unique au serveur d’images configuré avec le type de lecteur et les informations de version.

## Suivi personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour intégrer des systèmes d’analyse tiers, il est nécessaire d’écouter le rappel de la `trackEvent` visionneuse et de traiter l’ `eventInfo` argument de la fonction de rappel si nécessaire. Le code suivant est un exemple de cette fonction de gestionnaire :

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
   <td colname="col1"> <p> <span class="codeph"> PERMUTATION </span> </p> </td> 
   <td colname="col2"> <p>une ressource est permutée dans le lecteur à l’aide de l’ <span class="codeph"> API setAsset() </span> . </p> </td> 
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
   <td colname="col2"> <p> une image est modifiée en cliquant ou en appuyant sur une nuance. </p> </td> 
  </tr> 
 </tbody> 
</table>

