---
description: Référence de l’API JavaScript pour la visionneuse de zoom de base.
solution: Experience Manager
title: BasicZoomViewer
feature: Dynamic Media Classic, Visionneuses, SDK/API, Zoom
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---


# BasicZoomViewer{#basiczoomviewer}

Référence de l’API JavaScript pour la visionneuse de zoom de base.

`BasicZoomViewer([config])`

Constructeur, crée une nouvelle instance de visionneuse de zoom de base.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} objet de configuration JSON  </span> facultatif, permet à tous les paramètres de la visionneuse de passer au constructeur pour éviter d'appeler des méthodes de définition individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID du conteneur DOM (normalement un  <span class="codeph"> DIV  </span>) dans lequel le lecteur est inséré. Au moment de l’appel de cette méthode, il n’est pas nécessaire de créer l’élément de conteneur. Cependant, le conteneur doit exister lorsque <span class="codeph"> init() </span> est exécuté. Obligatoire. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params  </span> - Objet  <span class="codeph"> {Object}  </span> JSON avec des paramètres de configuration de visionneuse où le nom de la propriété est soit une option de configuration spécifique à la visionneuse, soit un modificateur SDK, et où la valeur de cette propriété est une valeur de paramètres correspondante. Obligatoire. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> gestionnaires  </span> -  <span class="codeph"> {Object} objet  </span> JSON avec rappels de événement de visionneuse, où le nom de propriété est le nom du événement de visionneuse pris en charge et la valeur de propriété est une référence de fonction JavaScript au rappel approprié. Facultatif. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local"> Rappels de Événement </a> pour plus d’informations sur les événements des lecteurs. </p> </li> 
      <li id="li_528FE03845F847E08F964E38D6AB6E86"> <p> <span class="codeph"> localizedTexts  </span> - Objet  <span class="codeph"> JSON  </span> {Object} avec données de localisation. Facultatif. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localisation des éléments de l’interface utilisateur </a> pour plus d’informations. </p> <p> Voir également le <i>Guide de l’utilisateur du kit de développement logiciel de visionneuse</i> et l’exemple pour plus d’informations sur le contenu de l’objet. Facultatif </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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

