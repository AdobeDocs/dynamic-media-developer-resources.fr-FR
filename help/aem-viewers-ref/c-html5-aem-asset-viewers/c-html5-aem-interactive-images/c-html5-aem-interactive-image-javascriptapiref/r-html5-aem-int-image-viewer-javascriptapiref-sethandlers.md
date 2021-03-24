---
description: Référence de l’API JavaScript pour la visionneuse d’images interactive
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic, Visionneuses, SDK/API, Images interactives
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---


# setHandlers{#sethandlers}

Référence de l’API JavaScript pour la visionneuse d’images interactive

`setHandlers(handlers)`

Spécifie zéro ou plusieurs gestionnaires de rappel. Un appel à cette méthode remplace complètement les gestionnaires de événement précédemment affectés pour cette instance de lecteur. Doit être appelé avant `init()`.

## Paramètre {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestionnaires  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Objet {Object}  </span> JSON avec rappels de événement de la visionneuse. Le nom de la propriété correspond au nom du événement de la visionneuse prise en charge. La valeur de propriété est une référence de fonction JavaScript à un rappel approprié. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Rappels de Événement </a> pour plus d’informations sur les événements des lecteurs. </p> </td> 
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

