---
description: L'indicateur de rotation est superposé sur la zone de vue principale. Elle s’affiche lorsque l’image est à l’état reset et dépend également du paramètre iconeffect.
seo-description: L'indicateur de rotation est superposé sur la zone de vue principale. Elle s’affiche lorsque l’image est à l’état reset et dépend également du paramètre iconeffect.
seo-title: Effet Icône
solution: Experience Manager
title: Effet Icône
topic: Dynamic Media
uuid: ce0524e4-fff4-45b0-8069-d5876802d66f
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---


# Effet Icône{#icon-effect}

L&#39;indicateur de rotation est superposé sur la zone de vue principale. Elle s’affiche lorsque l’image est à l’état reset et dépend également du paramètre iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visualisation principale**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7spinviewer .s7spinview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p> Illustration de l’indicateur de rotation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’indicateur de rotation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’indicateur de rotation. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’indicateur de rotation prend en charge le sélecteur d’attributs `state` qui est défini sur `spin_1D` dans le cas d’une visionneuse à 360° unidimensionnelle et sur `spin_2D` dans le cas d’une visionneuse à 360° multidimensionnelle.

Exemple : pour configurer un indicateur de zoom de 100 x 100 pixels.

```
.s7spinviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```

