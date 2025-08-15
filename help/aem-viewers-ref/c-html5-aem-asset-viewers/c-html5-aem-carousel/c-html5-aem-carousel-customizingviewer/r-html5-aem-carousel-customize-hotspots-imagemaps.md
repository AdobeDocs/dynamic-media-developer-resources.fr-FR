---
title: Zones réactives et zones cliquables
description: La visionneuse affiche des icônes de zone réactive sur la vue principale aux endroits où les zones réactives ont été créées à l’origine dans Dynamic Media d’AEM Assets – à la demande.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# Zones réactives et zones cliquables{#hotspots-and-image-maps}

La visionneuse affiche des icônes de zone réactive sur la vue principale aux endroits où les zones réactives ont été créées à l’origine dans Dynamic Media d’AEM Assets – à la demande.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone principale de la visionneuse**

L’apparence de l’icône de zone réactive est contrôlée par le sélecteur de classe CSS suivant :

```
.s7carouselviewer .s7imagemapeffect .s7icon
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Illustration de l’icône de zone réactive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône de zone réactive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône de zone réactive. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez une icône de zone réactive de 56 x 56 pixels qui affiche une image différente pour chacun des deux états d’icône :

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**Propriétés CSS de la région de zone cliquable**

L’aspect de la zone de zone cliquable est contrôlé par le sélecteur de classe CSS suivant :

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur de remplissage de zone cliquable. </p> <p>Spécifiez cette couleur aux <span class="codeph"> formats #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span>ou <span class="codeph"> RGBA(R,G,B,A). </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur de remplissage de zone cliquable. </p> <p>Spécifiez cette couleur aux <span class="codeph"> formats #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span>ou <span class="codeph"> RGBA(R,G,B,A). </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> frontière </span> </p> </td> 
   <td colname="col2"> <p> Style de bordure de zone de zone cliquable. Doit être spécifié comme " <span class="codeph"> largeur </span> <span class="codeph"> couleur unie </span>« , où <span class="codeph"> la largeur </span> est exprimée en pixels, et <span class="codeph"> la couleur </span> est définie comme <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB (R, G, B) </span>ou <span class="codeph"> RGBA (R, G, B, A). </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Configurez une zone de zone cliquable transparente avec une bordure noire d’un pixel :

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
