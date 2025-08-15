---
title: Bouton Zoom avant
description: Le fait de sélectionner ce bouton effectue un zoom avant sur une image dans la vue principale. Ce bouton apparaît dans la barre de contrôle principale. Ce bouton ne s’affiche pas sur les téléphones mobiles pour économiser l’espace de l’écran. Vous pouvez redimensionner, habiller et positionner ce bouton à l’aide de CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: b9d037fd-7ae3-424e-b9c7-c46a7d219127
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Bouton Zoom avant{#zoom-in-button}

Le fait de sélectionner ce bouton effectue un zoom avant sur une image dans la vue principale. Ce bouton apparaît dans la barre de contrôle principale. Ce bouton n&#39;est pas affiché sur les téléphones mobiles pour économiser l&#39;espace de l&#39;écran. Vous pouvez dimensionner, habiller et positionner ce bouton à l’aide de CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect du bouton est contrôlé avec le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7zoominbutton`

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
   <td colname="col1"> <p> <span class="codeph"> Droite </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite de la barre de contrôle principale, y compris la rembourrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Gauche </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état donné du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple - Pour configurer un bouton de zoom avant de 28 x 28 pixels, positionné à 4 pixels du bas et à 103 pixels du bord droit de la barre de contrôle principale. Enfin, affiche une image différente pour chacun des quatre états de bouton différents.

```
.s7ecatalogsearchviewer .s7zoominbutton { 
bottom:4px; 
right:103px; 
width:28px; 
height:28px; 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='up'] { 
background-image:url(images/v2/ZoomInButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='disabled'] { 
background-image:url(images/v2/ZoomInButton_dark_disabled.png); 
}
```
