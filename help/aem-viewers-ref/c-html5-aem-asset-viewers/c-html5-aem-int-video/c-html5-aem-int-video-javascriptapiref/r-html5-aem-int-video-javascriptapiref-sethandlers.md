---
description: Référence de l’API JavaScript pour la visionneuse de vidéos interactive
seo-description: Référence de l’API JavaScript pour la visionneuse de vidéos interactive
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic Media
uuid: f33df5a9-e323-4dff-b792-88d778332c75
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---


# setHandlers{#sethandlers}

Référence de l’API JavaScript pour la visionneuse de vidéos interactive

`setHandlers(handlers)`

Spécifie zéro ou plusieurs gestionnaires de rappel. Un appel à cette méthode remplace complètement les gestionnaires de événement précédemment affectés pour cette instance de lecteur. Doit être appelé avant `init()`.

## Paramètre {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestionnaires  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Objet {Object}  </span> JSON avec rappels de événement de visionneuse, où le nom de la propriété est le nom du événement de visionneuse pris en charge et où la valeur de la propriété est une référence de fonction JavaScript à un rappel approprié. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Rappels de Événement </a> pour plus d’informations sur les événements des lecteurs. </p> </td> 
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

