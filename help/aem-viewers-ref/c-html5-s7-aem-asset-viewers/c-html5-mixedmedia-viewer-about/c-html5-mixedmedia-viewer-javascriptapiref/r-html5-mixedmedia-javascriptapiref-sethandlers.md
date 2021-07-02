---
description: Référence de l’API JavaScript pour la visionneuse de supports variés.
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: e30f1b73-1dba-4d4c-9e90-f343ca404550
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# setHandlers{#sethandlers}

Référence de l’API JavaScript pour la visionneuse de supports variés.

`setHandlers(handlers)`

Spécifie zéro ou plusieurs gestionnaires de rappel. Un appel à cette méthode remplace complètement les gestionnaires d’événements précédemment affectés à cette instance de visionneuse. Doit être appelé avant `init()`.

## Paramètre {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestionnaires  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} Objet  </span> JSON avec rappels d’événement de visionneuse, où le nom de propriété est le nom de l’événement de visionneuse pris en charge et la valeur de la propriété est une référence de fonction JavaScript à un rappel approprié. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local"> Rappels d’événement </a> pour plus d’informations sur les événements de visionneuse. </p> </td> 
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
