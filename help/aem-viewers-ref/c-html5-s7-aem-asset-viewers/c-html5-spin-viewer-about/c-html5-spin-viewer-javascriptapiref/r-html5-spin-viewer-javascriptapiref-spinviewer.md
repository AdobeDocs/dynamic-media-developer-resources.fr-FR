---
title: SpinViewer
description: Référence de l’API JavaScript pour la visionneuse à 360°.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 0cfde665-c578-41a0-a428-0db3cbdac6ae
TQID: 'https://experienceleague.adobe.com/-aZhpoZiLqC8B77Ajt8wPTLBC3Z7zwcTiF9bPjndglg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 205
ht-degree: 3%

---

# SpinViewer{#spinviewer}

Référence de l’API JavaScript pour la visionneuse à 360°.

`SpinViewer([config])`

Constructeur, crée une instance Visionneuse à 360°.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objet de configuration JSON facultatif, permet à tous les paramètres de la visionneuse de passer au constructeur et d’éviter d’appeler des méthodes de définisseur individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} ID </span> conteneur DOM (normalement un </span> DIV <span class="codeph">) dans lequel la visionneuse est insérée. Il n’est pas nécessaire que l’élément de conteneur soit créé au moment où cette méthode est appelée. Cependant, le conteneur doit exister lors de <span class="codeph">’exécution de la </span> init(). Obligatoire. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params </span> - <span class="codeph"> objet {Object} </span> objet JSON avec des paramètres de configuration de visionneuse où le nom de la propriété est une option de configuration spécifique à la visionneuse ou un modificateur SDK et la valeur de cette propriété est une valeur de paramètres correspondante. Obligatoire. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> gestionnaires </span> - <span class="codeph"> {Object} </span> objet JSON avec des rappels d’événement de visionneuse, où le nom de la propriété est le nom de l’événement de visionneuse pris en charge et la valeur de la propriété est une référence de fonction JavaScript à un rappel approprié. Facultatif. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> des rappels d’événement </a> pour plus d’informations sur les événements de visionneuse. </p> </li> 
      <li id="li_643787FB4A424D0AB6B8E12F44C3A9AC"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> objet JSON avec des données de localisation. Facultatif. </p> <p>Pour plus d’informations, consultez <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> section Localisation des éléments de l’interface utilisateur </a> . </p> <p>Consultez également le <i>Guide d’utilisation de la visionneuse SDK</i> et l’exemple pour plus d’informations sur le contenu de l’objet . </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```
