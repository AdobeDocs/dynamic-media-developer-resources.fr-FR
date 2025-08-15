---
title: Bouton Page précédente
description: L’utilisateur clique ou appuie sur ce bouton pour revenir à la page précédente du catalogue. Ce bouton apparaît dans la barre de contrôle principale. Ce bouton ne s’affiche pas sur les téléphones mobiles pour économiser l’espace de l’écran. Vous pouvez redimensionner, habiller et positionner ce bouton à l’aide de CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: cc0e8c18-f9c1-4451-9fbe-3b082f78a7ec
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Bouton Page précédente{#previous-page-button}

Lorsque vous sélectionnez ou appuyez sur ce bouton, l’utilisateur arrive à la page précédente du catalogue. Ce bouton apparaît dans la barre de contrôle principale. Ce bouton ne s’affiche pas sur les téléphones mobiles pour économiser l’espace de l’écran. Vous pouvez redimensionner, habiller et positionner ce bouton à l’aide de CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Propriétés CSS de la zone principale de la visionneuse**

L’aspect du bouton est contrôlé par le sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton`

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
   <td colname="col2"> <p>Position à partir de la bordure supérieure de la barre de contrôle principale, y compris la rembourrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Droite </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite de la barre de contrôle principale, y compris la rembourrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Gauche </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure gauche de la barre de contrôle principale, y compris la remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure de la barre de contrôle principale, y compris la remplissage. </p> </td> 
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
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

Exemple : pour configurer un bouton Page précédente de 28 x 28 pixels et positionné à 4 pixels du bas et à 250 pixels du bord droit de la barre de contrôle principale. Enfin, affiche une image différente pour chacun des quatre états différents du bouton.

```
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton { 
bottom:4px; 
left:250px; 
width:32px; 
height:32px; 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/ToolBarLeftButton_dark_up.png); 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/ToolBarLeftButton_dark_over.png); 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/ToolBarLeftButton_dark_down.png); 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/ToolBarLeftButton_dark_disabled.png); 
}
```
