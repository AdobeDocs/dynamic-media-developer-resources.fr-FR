---
description: Référence de l’API JavaScript pour la visionneuse déroulante.
seo-description: Référence de l’API JavaScript pour la visionneuse déroulante.
seo-title: FlyoutViewer
solution: Experience Manager
title: FlyoutViewer
topic: Dynamic Media
uuid: 070ae248-34fd-40fb-9d40-2c7fff388592
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---


# FlyoutViewer{#flyoutviewer}

Référence de l’API JavaScript pour la visionneuse déroulante.

`FlyoutViewer([config])`

Constructeur; crée une instance de visionneuse Fenêtre déroulante.

## Paramètres {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} objet de configuration JSON  </span> facultatif, permet à tous les paramètres de la visionneuse de passer au constructeur et d'éviter d'appeler des méthodes de définition individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID du conteneur DOM (normalement un  <span class="codeph"> DIV  </span>) dans lequel le lecteur est inséré. Il n’est pas nécessaire de créer l’élément de conteneur au moment de l’appel de cette méthode. Cependant, le conteneur doit exister lorsque <span class="codeph"> init() </span> est exécuté. Obligatoire. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params  </span> - Objet  <span class="codeph"> {Object}  </span> JSON avec des paramètres de configuration de visionneuse où le nom de la propriété est soit une option de configuration spécifique à la visionneuse, soit un modificateur SDK, et où la valeur de cette propriété est une valeur de paramètres correspondante. Obligatoire. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> gestionnaires  </span> -  <span class="codeph"> {Object} objet  </span> JSON avec rappels de événement de visionneuse, où le nom de propriété est le nom du événement de visionneuse pris en charge et où la valeur de propriété est une référence de fonction JavaScript à un rappel approprié. Facultatif. <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> Rappels de Événement </a> pour plus d’informations sur les événements des lecteurs. </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts  </span> - {  <span class="codeph"> Object  </span>} objet JSON avec des données de localisation. Facultatif. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Localisation des éléments de l’interface utilisateur </a> pour plus d’informations. </p> <p>Pour plus d’informations sur le contenu de l’objet, consultez le <i>Guide de l’utilisateur du kit de développement de visionneuse</i> et l’exemple. Facultatif. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```

