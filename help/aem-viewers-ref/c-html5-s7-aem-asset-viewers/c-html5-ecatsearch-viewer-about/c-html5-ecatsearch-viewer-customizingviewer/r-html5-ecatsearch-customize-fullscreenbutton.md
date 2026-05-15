---
title: bouton plein écran
description: Fait passer la visionneuse en mode plein écran ou la fait quitter ce mode lorsqu’elle est sélectionnée par l’utilisateur. Ce bouton apparaît dans la barre de contrôle principale. Ce bouton ne s’affiche pas si la visionneuse fonctionne en mode pop-up et que le système ne prend pas en charge le plein écran natif. Vous pouvez dimensionner, appliquer une enveloppe et positionner le bouton par CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: a4b6fdc0-1047-46c6-bf77-4536819b7fcd
TQID: 'https://experienceleague.adobe.com/g9lccgpmTbJ9eQXlz2MMlfJfhCRRSLPjdLgR1CDwpv0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 330
ht-degree: 0%

---

# bouton plein écran{#full-screen-button}

Fait passer la visionneuse en mode plein écran ou la fait quitter ce mode lorsqu’elle est sélectionnée par l’utilisateur. Ce bouton apparaît dans la barre de contrôle principale. Ce bouton ne s’affiche pas si la visionneuse fonctionne en mode pop-up et que le système ne prend pas en charge le plein écran natif. Vous pouvez dimensionner, appliquer une enveloppe et positionner le bouton par CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect du bouton est contrôlé avec le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7fullscreenbutton`

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
   <td colname="col1"> <p> </span> inférieur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure de la barre de contrôle principale, y compris la marge intérieure. </p> </td> 
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
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge les sélecteurs d&#39;attributs `state` et `selected`, qui peuvent être utilisés pour appliquer différents habillages à différents états de bouton. En particulier, `selected='true'` correspond à l&#39;état « plein écran » et `selected='false'` correspond à l&#39;état « normal ».

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple - Pour configurer un bouton plein écran de 28 x 28 pixels positionné à 4 pixels du bas et à 5 pixels du bord droit de la barre de contrôle principale. Enfin, affiche une image différente pour chacun des quatre états de bouton différents, qu’ils soient sélectionnés ou non.

```
.s7ecatalogsearchviewer .s7fullscreenbutton { 
bottom:4px; 
right:5px; 
width:28px; 
height:28px; 
} 
.s7ecatalogsearchviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7ecatalogsearchviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7ecatalogsearchviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7ecatalogsearchviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7ecatalogsearchviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7ecatalogsearchviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7ecatalogsearchviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7ecatalogsearchviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
