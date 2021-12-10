---
title: ZoomViewer
description: Référence de l’API JavaScript pour la visionneuse de zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: fa52a017-0748-4e4f-8d91-ad1529fbfbdb
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---

# ZoomViewer{#zoomviewer}

Référence de l’API JavaScript pour la visionneuse de zoom.

`ZoomViewer([config])`

Constructeur, crée une instance Visionneuse de zoom.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> objet de configuration JSON facultatif, permet à tous les paramètres de visionneuse de transmettre au constructeur afin d’éviter d’appeler des méthodes de visionneuse individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID du conteneur DOM (généralement un <span class="codeph"> DIV </span>) dans laquelle la visionneuse est insérée. Au moment de l’appel de cette méthode, il n’est pas nécessaire de créer l’élément de conteneur. Cependant, le conteneur doit exister lorsque <span class="codeph"> init() </span> est exécuté. Obligatoire. </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> Objet JSON avec des paramètres de configuration de visionneuse pour lequel le nom de propriété est soit une option de configuration spécifique à la visionneuse, soit un modificateur SDK, et la valeur de cette propriété est une valeur de paramètres correspondante. Obligatoire. </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <span class="codeph"> gestionnaires </span> - <span class="codeph"> {Object} </span> Objet JSON avec rappels d’événement de visionneuse, où le nom de la propriété est le nom de l’événement de visionneuse pris en charge et où la valeur de la propriété est une référence de fonction JavaScript au rappel approprié. Facultatif. <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Rappels d’événement </a> pour plus d’informations sur les événements de visionneuse. </p> </li> 
      <li id="li_1D181A6B1D434B29B09AFD3F4BE059BD"> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> Objet JSON contenant des données de localisation. Facultatif. <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localisation des éléments de l’interface utilisateur </a> pour plus d’informations. </p> <p>Voir aussi <i>Guide de l’utilisateur du SDK de la visionneuse</i> et l’exemple pour plus d’informations sur le contenu de l’objet. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var zoomViewer = new s7viewers.ZoomViewer({ 
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
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```
