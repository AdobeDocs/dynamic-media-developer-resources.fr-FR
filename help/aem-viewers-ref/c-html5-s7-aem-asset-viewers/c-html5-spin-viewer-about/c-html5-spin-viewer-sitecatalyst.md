---
title: Prise en charge du suivi Adobe Analytics
description: La visionneuse à 360° prend en charge Adobe Analytics suivi par défaut.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User,Data Engineer,Data Architect
exl-id: 30762700-6d69-4299-9492-57893232abe1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse à 360° prend en charge Adobe Analytics suivi par défaut.

## Tracking d’usine {#section-d06145cfa2b9491bb485b599368d466e}

La visionneuse à 360° prend en charge le suivi Adobe Analytics prête-à-l’emploi.

Pour activer le suivi, transmettez le nom du paramètre prédéfini de la société en tant que `config2` paramètre.

La visionneuse envoie également une requête HTTP de suivi unique au serveur d’images configuré avec le type et les informations de version de la visionneuse.

## Suivi personnalisé {#section-47512156a1d64b338b50cfa39c84f4aa}

Pour l’intégration avec des systèmes d’analyse tiers, il est nécessaire d’écouter le `trackEvent` rappel du spectateur et de traiter l’argument `eventInfo` de la fonction de rappel, si nécessaire. Le code suivant est un exemple de fonction de gestionnaire :

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
   <td colname="col2"> <p>une ressource est permutée dans la visionneuse à l’aide de l’API <span class="codeph"> setAsset(). </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> L’image est agrandie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>Une image fait l’objet d’un panoramique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FILER </span> </p> </td> 
   <td colname="col2"> <p> Une rotation est effectuée. </p> </td> 
  </tr> 
 </tbody> 
</table>
