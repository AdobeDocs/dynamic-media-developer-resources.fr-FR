---
description: Référence de l’API JavaScript pour Carousel Viewer.
solution: Experience Manager
title: CarouselViewer
feature: Dynamic Media Classic, Visionneuses, SDK/API, Bannières de carrousel
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 3%

---


# CarouselViewer{#carouselviewer}

Référence de l’API JavaScript pour Carousel Viewer.

`CarouselViewer([config])`

Constructeur, crée une nouvelle instance de visionneuse de carrousel HTML 5.

## Paramètres {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} objet de configuration JSON  </span> facultatif, permet à tous les paramètres de la visionneuse de passer au constructeur pour éviter d'appeler des méthodes de définition individuelles. Contient les propriétés suivantes : </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID du conteneur DOM (normalement un  <span class="codeph"> DIV  </span>) dans lequel le lecteur est inséré. Au moment de l’appel de cette méthode, il n’est pas nécessaire de créer l’élément de conteneur. Cependant, le conteneur doit exister lorsque <span class="codeph"> init() </span> est exécuté. </p> <p>Obligatoire. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params  </span> - Objet  <span class="codeph"> {Object}  </span> JSON avec des paramètres de configuration de visionneuse où le nom de la propriété est soit une option de configuration spécifique à la visionneuse, soit un modificateur SDK, et où la valeur de cette propriété est une valeur de paramètres correspondante. </p> <p>Obligatoire. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> gestionnaires  </span> -  <span class="codeph"> {Object} objet  </span> JSON avec rappels de événement de visionneuse, où le nom de propriété est le nom du événement de visionneuse pris en charge et la valeur de propriété est une référence de fonction JavaScript au rappel approprié. </p> <p>Facultatif. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Rappels de Événement </a> pour plus d’informations sur les événements des lecteurs. </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> localizedTexts  </span> -  <span class="codeph"> {Object}  </span> </p> <p> Objet JSON avec données de localisation. Voir Localisation des éléments de l’interface utilisateur et l’exemple pour plus d’informations sur le contenu de l’objet. </p> <p>Facultatif </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left" 
}, 
"fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste" 
}, 
defaultLocale:"en" 
} 
});
```

