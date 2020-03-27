---
description: La visionneuse à 360° prend en charge le suivi Adobe Analytics en standard.
seo-description: La visionneuse à 360° prend en charge le suivi Adobe Analytics en standard.
seo-title: Prise en charge du suivi d’Adobe Analytics
solution: Experience Manager
title: Prise en charge du suivi d’Adobe Analytics
topic: Dynamic media
uuid: 337671f0-22e8-4e3e-a0a9-ce49d271ea56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge du suivi d’Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse à 360° prend en charge le suivi Adobe Analytics en standard.

## Suivi prêt à l’emploi {#section-d06145cfa2b9491bb485b599368d466e}

La visionneuse à 360° prend en charge le suivi prêt à l’emploi d’Adobe Analytics.

Pour activer le suivi, transmettez le nom de  prédéfini approprié comme `config2` paramètre.

Le lecteur envoie également une requête HTTP de suivi unique au serveur d’images configuré avec le type de lecteur et les informations de version.

## Suivi personnalisé {#section-47512156a1d64b338b50cfa39c84f4aa}

Pour intégrer des systèmes d’analyse tiers, il est nécessaire d’écouter le rappel du `trackEvent` lecteur et de traiter l’ `eventInfo` argument de la fonction de rappel, le cas échéant. Le code suivant est un exemple de cette fonction de gestionnaire :

```
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
   <td colname="col2"> <p>est chargé en premier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PERMUTATION </span> </p> </td> 
   <td colname="col2"> <p>une ressource est permutée dans le lecteur à l’aide de l’ <span class="codeph"> API setAsset() </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> une image est agrandie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PANORAMIQUE </span> </p> </td> 
   <td colname="col2"> <p>une image est numérisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ROTATION </span> </p> </td> 
   <td colname="col2"> <p> une rotation est effectuée. </p> </td> 
  </tr> 
 </tbody> 
</table>

