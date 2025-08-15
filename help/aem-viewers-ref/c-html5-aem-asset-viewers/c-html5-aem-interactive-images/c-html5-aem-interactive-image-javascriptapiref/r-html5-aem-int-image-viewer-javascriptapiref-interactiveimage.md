---
title: InteractiveImage
description: Référence de l’API JavaScript pour la visionneuse d’images vidéo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 165de14f-0031-4969-9671-5da310d44c28
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 3%

---

# InteractiveImage{#interactiveimage}

Référence de l’API JavaScript pour la visionneuse d’images vidéo.

`InteractiveImage([config])`

Constructeur, crée une instance Visionneuse d’images vidéo.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> objet de configuration JSON facultatif, permet à tous les paramètres de la visionneuse d’être transmis au constructeur pour éviter d’appeler des méthodes setter individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} ID </span> conteneur DOM (normalement un <span class="codeph"> DIV </span>) dans lequel la visionneuse est insérée. Lorsque cette méthode est appelée, il n’est pas nécessaire de créer l’élément de conteneur . Cependant, le conteneur doit exister lors de <span class="codeph">’exécution de la </span> init(). </p> <p>Obligatoire. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> objet JSON avec des paramètres de configuration de la visionneuse où le nom de la propriété est une option de configuration spécifique à la visionneuse ou un modificateur SDK et la valeur de cette propriété est une valeur de paramètres correspondante. </p> <p>Obligatoire. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> des gestionnaires </span> - <span class="codeph"> {Object} </span> objet JSON avec des rappels d’événement de visionneuse, où le nom de la propriété est le nom de l’événement de visionneuse pris en charge et la valeur de la propriété est une référence de fonction JavaScript au rappel approprié. </p> <p>Facultatif. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> des rappels d’événement </a> pour plus d’informations sur les événements de visionneuse. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
} 
});
```
