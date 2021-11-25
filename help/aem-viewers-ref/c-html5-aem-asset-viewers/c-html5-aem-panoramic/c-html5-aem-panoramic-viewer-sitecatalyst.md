---
title: Prise en charge du suivi Adobe Analytics
description: Prise en charge du suivi Adobe Analytics
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 1%

---

# Prise en charge du suivi Adobe Analytics{#support-for-adobe-analytics-tracking}

Par défaut, la visionneuse envoie une requête HTTP de suivi unique au serveur d’images configuré avec le type de visionneuse et les informations de version.

## Suivi personnalisé {#section-cda48fc9730142d0bb3326bac7df3271}

Pour s’intégrer au système d’analyse tiers, il est nécessaire d’écouter `trackEvent` rappel et processus de visionneuse `eventInfo` de la fonction de rappel, le cas échéant. Le code suivant est un exemple de fonction de gestionnaire de ce type :

```
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
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
   <th colname="col2" class="entry"> <p>Envoyé... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CHARGEMENT </span> </p> </td> 
   <td colname="col2"> <p>lorsque la visionneuse est chargée en premier. </p> </td> 
  </tr> 
 </tbody> 
</table>
