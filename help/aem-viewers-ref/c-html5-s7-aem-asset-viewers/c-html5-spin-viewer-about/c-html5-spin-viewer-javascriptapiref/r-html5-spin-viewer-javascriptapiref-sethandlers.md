---
description: Référence de l’API JavaScript pour la visionneuse à 360°
seo-description: Référence de l’API JavaScript pour la visionneuse à 360°
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 50db47ee-c1bb-4e45-bfcf-fae0fff6e0e8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setHandlers{#sethandlers}

Référence de l’API JavaScript pour la visionneuse à 360°

`setHandlers(handlers)`

Spécifie zéro ou plusieurs gestionnaires de rappel. Un appel à cette méthode remplace complètement les gestionnaires de  qui étaient précédemment affectés pour cette instance de lecteur. Doit être appelé avant `init()`.

## Paramètre {#section-51f820ded5e842bebd123e37a35176c7}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestionnaires </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Objet {Object} </span> JSON avec rappels de de visionneuse, où le nom de propriété est le nom du de visionneuse pris en charge et où la valeur de propriété est une référence de fonction JavaScript à un rappel approprié. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> Rappels de  </a> pour plus d’informations sur l’ du lecteur de contenu. </p> </td> 
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

