---
description: Les échantillons sont constitués d’une rangée d’images miniatures avec des boutons de défilement facultatifs à gauche et à droite. Les boutons de défilement ne sont visibles sur le bureau que si toutes les miniatures ne peuvent pas tenir dans la largeur  du. Sur les périphériques mobiles, ou si les miniatures peuvent s’ajuster à la largeur du  du, les boutons de défilement ne s’affichent pas.
seo-description: Les échantillons sont constitués d’une rangée d’images miniatures avec des boutons de défilement facultatifs à gauche et à droite. Les boutons de défilement ne sont visibles sur le bureau que si toutes les miniatures ne peuvent pas tenir dans la largeur  du. Sur les périphériques mobiles, ou si les miniatures peuvent s’ajuster à la largeur du  du, les boutons de défilement ne s’affichent pas.
seo-title: Echantillons
solution: Experience Manager
title: Echantillons
topic: Dynamic media
uuid: d44e775d-5253-4990-98a4-84ff50db09b9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Echantillons{#swatches}

Les échantillons sont constitués d’une rangée d’images miniatures avec des boutons de défilement facultatifs à gauche et à droite. Les boutons de défilement ne sont visibles sur le bureau que si toutes les miniatures ne peuvent pas tenir dans la largeur  du. Sur les périphériques mobiles, ou si les miniatures peuvent s’ajuster à la largeur du  du, les boutons de défilement ne s’affichent pas.

`.s7zoomviewer .s7swatches`

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect du de nuances est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7zoomviewer .s7zoomresetbutton
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur des nuances. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur des nuances. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Décalage des échantillons verticaux par rapport au  du lecteur de contenu. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer des nuances sur 460 x 100 pixels.

```
.s7zoomviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

L’espacement entre les miniatures d’échantillon est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7zoomviewer .s7swatches .s7thumbcell`

<table id="table_565B354FEA814804A0BE3978E1242110"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Taille de la marge horizontale et verticale autour de chaque miniature. L’espacement réel des miniatures est égal à la somme des marges gauche et droite définies pour <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**

Pour définir l’espacement sur 10 pixels tant verticalement qu’horizontalement.

```
.s7zoomviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

L’aspect de la miniature individuelle est contrôlé par le sélecteur de classe CSS suivant :

`.s7zoomviewer .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure de la vignette. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniature prend en charge le sélecteur d’ `state` attributs, qui peut être utilisé pour appliquer différents habillages à différents états de miniature. En particulier, `state="selected"` correspond à la miniature de l’image actuellement affichée dans le principal, `state="default"` correspond au reste des miniatures et `state="over"` est utilisée lorsque vous passez la souris dessus.

Exemple : pour configurer des miniatures de 56 x 56 pixels, utilisez une bordure par défaut gris clair et une bordure sélectionnée gris foncé.

```
.s7zoomviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7zoomviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7zoomviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

L’aspect des boutons de défilement gauche et droit est contrôlé par les sélecteurs de classe CSS suivants :

`.s7zoomviewer .s7swatches .s7scrollleftbutton`

`.s7zoomviewer .s7swatches .s7scrollrightbutton`

Il n’est pas possible de positionner les boutons de défilement à l’aide des propriétés CSS top, left, bottom et right. Au lieu de cela, la logique du lecteur les positionne automatiquement.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’ `state` attributs, qui peut être utilisé pour appliquer différents habillages à différents états de bouton : `up`, `down`, `over`et `disabled`.

Les info-bulles des boutons peuvent être localisées. Voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)de l’interface utilisateur.

Exemple : pour configurer des boutons de défilement de 56 x 56 pixels et présentant des illustrations différentes pour chaque état.

```
.s7zoomviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```

