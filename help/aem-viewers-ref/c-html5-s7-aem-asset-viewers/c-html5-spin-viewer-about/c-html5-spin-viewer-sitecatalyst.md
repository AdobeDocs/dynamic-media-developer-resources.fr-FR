---
title: Prise en charge du suivi Adobe Analytics
description: La visionneuse à 360° prend en charge le suivi Adobe Analytics prêt à l’emploi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User,Data Engineer,Data Architect
exl-id: 30762700-6d69-4299-9492-57893232abe1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse à 360° prend en charge le suivi Adobe Analytics prêt à l’emploi.

## Suivi d’usine {#section-d06145cfa2b9491bb485b599368d466e}

La visionneuse à 360° prend en charge le suivi Adobe Analytics prêt à l’emploi.

Pour activer le suivi, transmettez le nom de paramètre prédéfini d’entreprise approprié en tant que `config2` .

La visionneuse envoie également une requête HTTP de suivi unique au serveur d’images configuré avec le type de visionneuse et les informations de version.

## Suivi personnalisé {#section-47512156a1d64b338b50cfa39c84f4aa}

Pour s’intégrer à des systèmes d’analyse tiers, il est nécessaire d’écouter la `trackEvent` rappel de la visionneuse et traitement de la `eventInfo` de la fonction de rappel, selon les besoins. Le code suivant est un exemple de fonction de gestionnaire de ce type :

```javascript {.line-numbers}
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
   <td colname="col2"> <p>une ressource est permutée dans la visionneuse à l’aide de la fonction <span class="codeph"> setAsset() </span> API. </p> </td> 
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
