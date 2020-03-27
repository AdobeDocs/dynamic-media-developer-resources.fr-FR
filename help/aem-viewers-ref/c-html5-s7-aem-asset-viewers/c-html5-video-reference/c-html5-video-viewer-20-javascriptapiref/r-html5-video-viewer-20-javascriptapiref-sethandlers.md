---
description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 02535997-521f-420f-af0b-5c8ec0fe0876
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setHandlers{#sethandlers}

Référence de l’API JavaScript pour la visionneuse de vidéos.

`setHandlers(handlers)`

Spécifie zéro ou plusieurs gestionnaires de rappel. Un appel à cette méthode remplace complètement les gestionnaires de  qui étaient précédemment affectés pour cette instance de lecteur. Doit être appelé avant `init()`.

## Paramètre {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestionnaires </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Objet {Object} </span> JSON avec rappels de de visionneuse, où le nom de propriété est le nom du de visionneuse pris en charge et où la valeur de propriété est une référence de fonction JavaScript à un rappel approprié. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> Rappels de  </a> pour plus d’informations sur l’ du lecteur de contenu. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

