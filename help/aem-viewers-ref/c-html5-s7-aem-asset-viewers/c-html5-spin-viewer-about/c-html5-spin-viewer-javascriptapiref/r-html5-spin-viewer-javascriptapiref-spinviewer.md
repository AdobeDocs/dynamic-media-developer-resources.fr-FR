---
description: Référence de l’API JavaScript pour la visionneuse à 360°.
seo-description: Référence de l’API JavaScript pour la visionneuse à 360°.
seo-title: Visionneuse à 360°
solution: Experience Manager
title: Visionneuse à 360°
topic: Dynamic Media
uuid: e9048f17-7a2a-4eae-a5a0-df14f16aebc5
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---


# SpinViewer{#spinviewer}

Référence de l’API JavaScript pour la visionneuse à 360°.

`SpinViewer([config])`

Constructeur, crée une instance de visionneuse à 360°.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} objet de configuration JSON  </span> facultatif, permet à tous les paramètres de la visionneuse de passer au constructeur et d'éviter d'appeler des méthodes de définition individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID du conteneur DOM (normalement un  <span class="codeph"> DIV  </span>) dans lequel le lecteur est inséré. Il n’est pas nécessaire de créer l’élément de conteneur au moment de l’appel de cette méthode. Cependant, le conteneur doit exister lorsque <span class="codeph"> init() </span> est exécuté. Obligatoire. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params  </span> - Objet  <span class="codeph"> {Object}  </span> JSON avec des paramètres de configuration de visionneuse où le nom de la propriété est soit une option de configuration spécifique à la visionneuse, soit un modificateur SDK, et où la valeur de cette propriété est une valeur de paramètres correspondante. Obligatoire. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> gestionnaires  </span> -  <span class="codeph"> {Object} objet  </span> JSON avec rappels de événement de visionneuse, où le nom de propriété est le nom du événement de visionneuse pris en charge et où la valeur de propriété est une référence de fonction JavaScript à un rappel approprié. Facultatif. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> Rappels de Événement </a> pour plus d’informations sur les événements des lecteurs. </p> </li> 
      <li id="li_643787FB4A424D0AB6B8E12F44C3A9AC"> <p> <span class="codeph"> localizedTexts  </span> - Objet  <span class="codeph"> JSON  </span> {Object} avec données de localisation. Facultatif. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> Localisation des éléments de l’interface utilisateur </a> pour plus d’informations. </p> <p>Voir également le <i>Guide de l’utilisateur du kit de développement logiciel de visionneuse</i> et l’exemple pour plus d’informations sur le contenu de l’objet. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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

