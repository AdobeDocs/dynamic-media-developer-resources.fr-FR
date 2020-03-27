---
description: Référence de l’API JavaScript pour la visionneuse d’images vidéo.
seo-description: Référence de l’API JavaScript pour la visionneuse d’images vidéo.
seo-title: InteractiveImage
solution: Experience Manager
title: InteractiveImage
topic: Dynamic media
uuid: 19bd0603-3180-4913-b5a0-93699c5131bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# InteractiveImage{#interactiveimage}

Référence de l’API JavaScript pour la visionneuse d’images vidéo.

`InteractiveImage([config])`

Constructeur, crée une nouvelle instance de visionneuse d’images vidéo.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> , objet de configuration JSON facultatif, permet à tous les paramètres de la visionneuse de transmettre au constructeur afin d’éviter d’appeler des méthodes de définition individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID du DOM (normalement un <span class="codeph"> DIV </span>) dans lequel le lecteur est inséré. Au moment de l’appel de cette méthode, il n’est pas nécessaire de créer l’élément  de. Cependant, le  doit exister lorsque <span class="codeph"> init() </span> est exécuté. </p> <p>Obligatoire. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - Objet <span class="codeph"> {Object} </span> JSON avec paramètres de configuration de la visionneuse dans lequel le nom de la propriété est soit une option de configuration spécifique à la visionneuse, soit un modificateur SDK, et la valeur de cette propriété est une valeur de paramètres correspondante. </p> <p>Obligatoire. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> gestionnaires </span> - Objet <span class="codeph"> {Object} </span> JSON avec rappels de de visionneuse, où le nom de propriété est le nom du de visionneuse pris en charge et où la valeur de propriété est une référence de fonction JavaScript au rappel approprié. </p> <p>Facultatif. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Rappels de  </a> pour plus d’informations sur l’ du lecteur de contenu. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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

