---
title: Bouton Dernière page
description: Lorsque vous sélectionnez ce bouton, l’utilisateur arrive à la dernière page du catalogue. Ce bouton apparaît dans la barre de contrôle principale sur les systèmes de bureau et les tablettes ; Sur les téléphones mobiles, il est ajouté à une barre de contrôle secondaire. Vous pouvez redimensionner, habiller et positionner ce bouton à l’aide de CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa1ff52c-6fb1-47e7-b3d4-216fea02bbd8
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Bouton Dernière page{#last-page-button}

Lorsque vous sélectionnez ce bouton, l’utilisateur arrive à la dernière page du catalogue. Ce bouton apparaît dans la barre de contrôle principale sur les systèmes de bureau et les tablettes ; Sur les téléphones mobiles, il est ajouté à une barre de contrôle secondaire. Vous pouvez redimensionner, habiller et positionner ce bouton à l’aide de CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Propriétés CSS de la zone principale de la visionneuse**

L’aspect du bouton est contrôlé par le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7lastpagebutton .s7panleftbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure de la barre de contrôle principale (sur les ordinateurs de bureau et les tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Droite </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite de la barre de contrôle principale (sur les ordinateurs de bureau et les tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris la rembourrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Gauche </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure gauche de la barre de contrôle principale (sur les ordinateurs de bureau et les tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris la rembourrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure de la barre de contrôle principale (sur les ordinateurs de bureau et les tablettes) ou de la barre de contrôle secondaire (sur les téléphones mobiles), y compris la rembourrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état donné du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

Exemple : pour configurer un bouton Dernière page de 28 x 28 pixels et positionné à 4 pixels du bas et à 220 pixels du bord gauche de la barre de contrôle principale. Enfin, affiche une image différente pour chacun des quatre états différents du bouton.

```
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton { 
bottom:4px; 
right:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/LastPageButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/LastPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/LastPageButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/LastPageButton_dark_disabled.png); 
}
```
