---
title: Bouton Fermer
description: Sélectionner ou appuyer sur ce bouton ferme la page web qui le contient. Ce bouton n'apparaît que si le paramètre closebutton est défini sur 1. Vous pouvez dimensionner, habiller et positionner ce bouton à l’aide de CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8f466e8c-29a8-408d-97ae-e40043cb04e5
TQID: 'https://experienceleague.adobe.com/eUZCSSJd-UagUXHVdF1-GLpTQUtDeKCb-wMnjyDolNI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Bouton Fermer{#close-button}

Sélectionner ou appuyer sur ce bouton ferme la page web qui le contient. Ce bouton n&#39;apparaît que si le paramètre closebutton est défini sur 1. Vous pouvez dimensionner, habiller et positionner ce bouton à l’aide de CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect du bouton est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7zoomviewer .s7closebutton
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
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droit </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite, marge intérieure incluse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure gauche, marge intérieure incluse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> inférieur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exemple - Pour configurer un bouton Fermer de 32 x 32 pixels positionné à six pixels du bord supérieur et droit de la visionneuse. Enfin, affiche une image différente pour chacun des quatre états de bouton différents.

```
.s7zoomviewer .s7closebutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7zoomviewer .s7closebutton [state='up'] { 
background-image:url(images/v2/CloseButton_dark_up.png); 
} 
.s7zoomviewer .s7closebutton [state='over'] {  
background-image:url(images/v2/CloseButton_dark_over.png); 
} 
.s7zoomviewer .s7closebutton [state='down'] {  
background-image:url(images/v2/CloseButton_dark_down.png); 
} 
.s7zoomviewer .s7closebutton [state='disabled'] { 
background-image:url(images/v2/CloseButton_dark_disabled.png); 
}
```

