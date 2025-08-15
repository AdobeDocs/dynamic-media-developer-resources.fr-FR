---
title: Bouton Zoom arrière
description: Le fait de sélectionner ce bouton effectue un zoom arrière sur une image dans la vue principale. Ce bouton ne s'affiche pas sur les téléphones mobiles pour économiser de l'espace sur l'écran. Vous pouvez dimensionner, habiller et positionner ce bouton à l’aide de CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: a4c2eb32-819c-45a1-ac03-44e78ebd042b
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Bouton Zoom arrière{#zoom-out-button}

Le fait de sélectionner ce bouton effectue un zoom arrière sur une image dans la vue principale. Ce bouton ne s&#39;affiche pas sur les téléphones mobiles pour économiser de l&#39;espace sur l&#39;écran. Vous pouvez dimensionner, habiller et positionner ce bouton à l’aide de CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect du bouton est contrôlé avec le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7zoomoutbutton`

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
   <td colname="col2"> <p>Position à partir de la bordure supérieure de la barre de contrôle principale, marge intérieure incluse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droit </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite de la barre de contrôle principale, marge intérieure incluse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure gauche de la barre de contrôle principale, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inférieur </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure de la barre de contrôle principale, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple - Pour configurer un bouton de zoom arrière de 28 x 28 pixels, positionné à 4 pixels du bas et à 75 pixels du bord droit de la barre de contrôle principale. Enfin, affiche une image différente pour chacun des quatre états de bouton différents.

```
.s7ecatalogsearchviewer .s7zoomoutbutton { 
bottom:4px; 
right:75px; 
width:28px; 
height:28px; 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='up'] { 
background-image:url(images/v2/ZoomOutButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='over'] {  
background-image:url(images/v2/ZoomOutButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='down'] {  
background-image:url(images/v2/ZoomOutButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='disabled'] { 
background-image:url(images/v2/ZoomOutButton_dark_disabled.png); 
}
```
