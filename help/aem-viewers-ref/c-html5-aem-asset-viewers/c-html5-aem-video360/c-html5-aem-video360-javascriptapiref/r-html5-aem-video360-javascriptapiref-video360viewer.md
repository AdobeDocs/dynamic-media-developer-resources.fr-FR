---
description: Référence de l’API JavaScript pour le lecteur vidéo360.
seo-description: Référence de l’API JavaScript pour le lecteur vidéo360.
seo-title: Video360Viewer
solution: Experience Manager
title: Video360Viewer
topic: Dynamic media
uuid: b5d5e270-687c-40aa-9de4-c5bc2a7806f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Viewer{#video-viewer}

Référence de l’API JavaScript pour le lecteur vidéo360.

`Video360Viewer([config])`

Constructeur, crée une nouvelle instance de visionneuse de vidéos360 HTML5.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> , objet de configuration JSON facultatif, permet à tous les paramètres de la visionneuse de transmettre au constructeur afin d’éviter d’appeler des méthodes de définition individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID du DOM (normalement un <span class="codeph"> DIV </span>) dans lequel le lecteur est inséré. Au moment de l’appel de cette méthode, il n’est pas nécessaire de créer l’élément  de. Cependant, le  doit exister lorsque <span class="codeph"> init() </span> est exécuté. </p> <p>Obligatoire. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - Objet <span class="codeph"> {Object} </span> JSON avec paramètres de configuration de la visionneuse dans lequel le nom de la propriété est soit une option de configuration spécifique à la visionneuse, soit un modificateur SDK, et la valeur de cette propriété est une valeur de paramètres correspondante. </p> <p>Obligatoire. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> gestionnaires </span> - Objet <span class="codeph"> {Object} </span> JSON avec rappels de de visionneuse, où le nom de propriété est le nom du de visionneuse pris en charge et où la valeur de propriété est une référence de fonction JavaScript au rappel approprié. </p> <p>Facultatif. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Rappels de  </a> pour plus d’informations sur l’ du lecteur de contenu. </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedTexts </span> - Objet <span class="codeph"> {Object} </span> JSON avec données . Facultatif. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> des éléments de l’interface utilisateur </a> pour plus d’informations. </p> <p>Voir également le Guide <i>de l’utilisateur du kit de développement</i> de visionneuse et l’exemple pour plus d’informations sur le contenu de l’objet. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```

