---
description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-title: Visionneuse vidéo
solution: Experience Manager
title: Visionneuse vidéo
topic: Dynamic media
uuid: ad180d92-3e5c-4ded-b82b-79c23aa5c597
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Visionneuse vidéo{#videoviewer}

Référence de l’API JavaScript pour la visionneuse de vidéos.

`VideoViewer([config])`

Constructeur; crée une instance de visionneuse vidéo.

## Paramètres {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> , objet de configuration JSON facultatif, permet à tous les paramètres de la visionneuse de transmettre au constructeur et d’éviter d’appeler des méthodes de définition individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID du DOM (normalement un <span class="codeph"> DIV </span>) dans lequel le lecteur est inséré. Il n’est pas nécessaire que l’élément  soit créé au moment de l’appel de cette méthode. Cependant, le  doit exister lorsque <span class="codeph"> init() </span> est exécuté. Obligatoire. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - Objet <span class="codeph"> {Object} </span> JSON avec paramètres de configuration de la visionneuse, où le nom de propriété est soit une option de configuration spécifique à la visionneuse, soit un modificateur SDK, et où la valeur de cette propriété est une valeur de paramètres correspondante. Obligatoire. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> gestionnaires </span> - Objet <span class="codeph"> {Object} </span> JSON avec rappels de de visionneuse, où le nom de propriété est le nom du de visionneuse pris en charge  et où la valeur de propriété est une référence de fonction JavaScript à un rappel approprié. Facultatif. <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> Rappels de  </a> pour plus d’informations sur l’ du lecteur de contenu. </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Object </span>} objet JSON avec des données . Facultatif. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> SDK de lecteur  </a> pour plus d’informations. </p> <p>Pour plus d’informations sur le contenu de l’objet, consultez le Guide <i>de l’utilisateur du kit de développement de</i> visionneuse et l’exemple. Facultatif. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```

