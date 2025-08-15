---
title: Visionneuse de zoom de base
description: JavaScript référence de l’API pour la visionneuse de zoom de base.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 320f740e-c6b9-44d6-9369-9c2ec31189c5
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 3%

---

# Visionneuse de zoom de base{#basiczoomviewer}

JavaScript référence de l’API pour la visionneuse de zoom de base.

`BasicZoomViewer([config])`

Constructeur, crée une instance de base de la visionneuse de zoom.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> </span> Fichier de configuration </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">{object} </span> objet de configuration JSON facultatif, permet à tous les paramètres de visionneuse de passer au constructeur pour éviter d’appeler des méthodes de setter individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph">containerId </span> - <span class="codeph"> {String} </span> ID du conteneur DOM (normalement un <span class="codeph"> DIV</span>) dans lequel la visionneuse est insérée. Au moment où cette méthode est appelée, il n’est pas nécessaire de créer l’élément conteneur. Cependant, le conteneur doit exister lorsque <span class="codeph"> init() </span> est exécuté. Obligatoire. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> objet JSON avec des paramètres de configuration de visionneuse où le nom de la propriété est une option de configuration spécifique à la visionneuse ou un modificateur SDK, et la valeur de cette propriété est une valeur de paramètres correspondante. Obligatoire. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> Handlers </span> : <span class="codeph"> {Object} </span> objet JSON avec rappels d’événement de visionneuse, où le nom de la propriété est le nom de l’événement de visionneuse pris en charge et la valeur de la propriété est une référence de fonction JavaScript au rappel approprié. Facultatif. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local"> Rappels d’événement pour plus d’informations sur les </a> événements de visionneuse. </p> </li> 
      <li id="li_528FE03845F847E08F964E38D6AB6E86"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> objet JSON avec données de localisation. Facultatif. </p> <p>Pour plus d’informations, voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localisation des éléments </a> de l’interface utilisateur. </p> <p> Consultez également le Guide<i> de l’utilisateur </i>du Kit de développement logiciel (SDK) de la visionneuse et l’exemple pour plus d’informations sur le contenu de l’objet. Facultatif </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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
