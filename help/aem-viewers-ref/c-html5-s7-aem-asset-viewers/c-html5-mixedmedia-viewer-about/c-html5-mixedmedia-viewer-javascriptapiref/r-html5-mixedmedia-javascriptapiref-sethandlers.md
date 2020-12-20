---
description: Référence de l’API JavaScript pour la visionneuse de supports variés.
seo-description: Référence de l’API JavaScript pour la visionneuse de supports variés.
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 2477ec80-f627-48da-a66d-a86f17d7cc7d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---


# setHandlers{#sethandlers}

Référence de l’API JavaScript pour la visionneuse de supports variés.

`setHandlers(handlers)`

Spécifie zéro ou plusieurs gestionnaires de rappel. Un appel à cette méthode remplace complètement les gestionnaires de événement précédemment affectés pour cette instance de lecteur. Doit être appelé avant `init()`.

## Paramètre {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestionnaires  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Objet {Object}  </span> JSON avec rappels de événement de visionneuse, où le nom de la propriété est le nom du événement de visionneuse pris en charge et où la valeur de la propriété est une référence de fonction JavaScript à un rappel approprié. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local"> Rappels de Événement </a> pour plus d’informations sur les événements des lecteurs. </p> </td> 
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

