---
title: Prise en charge du suivi Adobe Analytics
description: La visionneuse de supports variés prend en charge le suivi Adobe Analytics prête-à-l’emploi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User,Data Engineer,Data Architect
exl-id: 3b28c853-3747-4805-a141-3cce1398d783
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

La visionneuse de supports variés prend en charge le suivi Adobe Analytics prête-à-l’emploi.

## Tracking d’usine {#section-ba994f079d0343c8ae48adffaa3195a3}

La visionneuse de supports variés prend en charge le [!DNL Adobe Analytics] suivi en standard. Pour activer le suivi, transmettez le nom du paramètre prédéfini de la société en tant que `config2` paramètre.

La visionneuse envoie également une requête HTTP de suivi unique au serveur d’images configuré avec le type et les informations de version de la visionneuse.

## Suivi personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour intégrer des systèmes d’analyse tiers, il est nécessaire d’écouter le rappel de la `trackEvent` visionneuse et de traiter l’argument `eventInfo` de la fonction de rappel si nécessaire. Le code suivant est un exemple de fonction de gestionnaire :

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
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>L’image est agrandie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>Une image fait l’objet d’un panoramique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ÉCHANTILLON </span> </p> </td> 
   <td colname="col2"> <p> Une image peut être modifiée en cliquant ou en appuyant sur un échantillon. </p> </td> 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FILER </span> </p> </td> 
   <td colname="col2"> <p>La rotation est exécutée. </p> </td> 
  </tr> 
 </tbody> 
</table>
