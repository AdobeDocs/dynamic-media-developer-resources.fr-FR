---
description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 33779874-2ab9-490a-8eaf-726adaa76327
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 3%

---

# setHandlers{#sethandlers}

Référence de l’API JavaScript pour la visionneuse de catalogue électronique.

[!DNL `setHandlers(handlers)`]

Spécifie aucun ou plusieurs gestionnaires de rappel. Un appel à cette méthode remplace complètement les gestionnaires d’événements précédemment affectés à cette instance de visionneuse. Doit être appelé avant `init()`.

## Paramètre {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestionnaires </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objet JSON avec des rappels d’événement de visionneuse, où le nom de la propriété est le nom de l’événement de visionneuse pris en charge et la valeur de la propriété est une référence de fonction JavaScript à un rappel approprié. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> des rappels d’événement </a> pour plus d’informations sur les événements de visionneuse. </p> </td> 
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
