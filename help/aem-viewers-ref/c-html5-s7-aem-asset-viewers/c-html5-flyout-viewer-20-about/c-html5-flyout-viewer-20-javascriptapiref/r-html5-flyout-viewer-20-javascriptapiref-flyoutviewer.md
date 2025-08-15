---
title: Visionneuse de fenêtre déroulante
description: JavaScript référence de l’API pour la visionneuse déroulante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b64f16c8-03bf-4603-972f-845a4c1e2b02
source-git-commit: f970421ccc482b698343aa18e7dfde7bea4c2a89
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 3%

---

# Visionneuse de fenêtre déroulante{#flyoutviewer}

JavaScript référence de l’API pour la visionneuse déroulante.

`FlyoutViewer([config])`

Constructeur; crée une instance de visionneuse de fenêtre déroulante.

## Paramètres {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> </span> Fichier de configuration </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">{Object} </span> objet de configuration JSON facultatif, permet à tous les paramètres de visionneuse de passer au constructeur et d’éviter d’appeler des méthodes de setter individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph">containerId </span> - <span class="codeph"> {String} </span> ID du conteneur DOM (normalement un <span class="codeph"> DIV</span>) dans lequel la visionneuse est insérée. Il n’est pas nécessaire que l’élément conteneur soit créé au moment de l’appel de cette méthode. Cependant, le conteneur doit exister lorsque <span class="codeph"> init() </span> est exécuté. Obligatoire. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> objet JSON avec des paramètres de configuration de visionneuse où le nom de la propriété est une option de configuration spécifique à la visionneuse ou un modificateur SDK, et la valeur de cette propriété est une valeur de paramètres correspondante. Obligatoire. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> Handlers </span> - <span class="codeph"> {Object} </span> Objet JSON avec rappels d’événement de visionneuse, où le nom de la propriété est le nom de l’événement de visionneuse pris en charge et la valeur de la propriété est une référence de fonction JavaScript à un rappel approprié. Facultatif. <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> Rappels d’événement pour plus d’informations sur les </a> événements de visionneuse. </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> object </span>} Objet JSON avec données de localisation. Facultatif. </p> <p>Pour plus d’informations, voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Localisation des éléments </a> de l’interface utilisateur. </p> <p>Voir le Guide<i> de l’utilisateur </i>du Kit de développement logiciel (SDK) de la visionneuse et l’exemple pour plus d’informations sur le contenu de l’objet. Facultatif. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
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
