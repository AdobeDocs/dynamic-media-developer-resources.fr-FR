---
title: setHandlers
description: Référence de l’API JavaScript pour la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 3%

---

# setHandlers{#sethandlers}

Référence de l’API JavaScript pour la visionneuse de vidéos avec recadrage intelligent.

`setHandlers(handlers)`

Spécifie zéro ou plusieurs gestionnaires de rappel. Un appel à cette méthode remplace complètement les gestionnaires d’événements précédemment affectés à cette instance de visionneuse. Doit être appelé avant `init()`.

## Paramètre {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestionnaires </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> Objet JSON avec rappels d’événement de visionneuse, où le nom de la propriété est le nom de l’événement de visionneuse pris en charge et où la valeur de la propriété est une référence de fonction JavaScript à un rappel approprié. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> Rappels d’événement </a> pour plus d’informations sur les événements de visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```
