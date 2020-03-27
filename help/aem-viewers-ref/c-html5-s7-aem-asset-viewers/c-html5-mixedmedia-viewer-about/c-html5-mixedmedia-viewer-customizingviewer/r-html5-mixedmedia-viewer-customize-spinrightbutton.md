---
description: Cliquez ou appuyez sur ce bouton pour faire tourner l’image vers la droite dans le  principal. Ce bouton n’est pas affiché sur les téléphones mobiles pour enregistrer l’espace sur l’écran. En outre, le bouton est masqué lorsqu’une visionneuse à 360° multidimensionnelle est utilisée. Vous pouvez dimensionner, habiller et positionner le bouton à l’aide de CSS.
seo-description: Cliquez ou appuyez sur ce bouton pour faire tourner l’image vers la droite dans le  principal. Ce bouton n’est pas affiché sur les téléphones mobiles pour enregistrer l’espace sur l’écran. En outre, le bouton est masqué lorsqu’une visionneuse à 360° multidimensionnelle est utilisée. Vous pouvez dimensionner, habiller et positionner le bouton à l’aide de CSS.
seo-title: Bouton de rotation à droite
solution: Experience Manager
title: Bouton de rotation à droite
topic: Dynamic media
uuid: 3af363bd-3de3-42c7-80cc-4512ffc1f10d
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Spin right button{#spin-right-button}

Cliquez ou appuyez sur ce bouton pour faire tourner l’image vers la droite dans le  principal. Ce bouton n’est pas affiché sur les téléphones mobiles pour enregistrer l’espace sur l’écran. En outre, le bouton est masqué lorsqu’une visionneuse à 360° multidimensionnelle est utilisée. Vous pouvez dimensionner, habiller et positionner le bouton à l’aide de CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS des boutons à 360°**

Le bouton est ajouté à un interne  dont la balise DIV est contrôlée par le sélecteur de classe CSS :

```
.s7mixedmediaviewer .s7spinbuttons
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
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure gauche, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’aspect de ce bouton à l’intérieur du  est contrôlé par le sélecteur de classe CSS :

```
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton
```

<table id="table_3EC45539877A479DB83E8FC69142450B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure gauche, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure inférieure, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’ `state` attributs, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

Les info-bulles des boutons peuvent être localisées. Pour plus d’informations, voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) de l’interface utilisateur.

Exemple : pour configurer un bouton de rotation droite de 28 x 28 pixels, positionné sur le bord droit du  intérieur, et affichant une image différente pour chacun des quatre états de bouton différents :

```
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton { 
 position:absolute; 
 right: 0px; 
 width:28px; 
 height:28px; 
 background-size:contain; 
 } 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='up'] { 
background-image:url(images/v2/SpinRightButton_light_up.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='over'] { 
background-image:url(images/v2/SpinRightButton_light_over.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='down'] { 
 background-image:url(images/v2/SpinRightButton_light_down.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='disabled'] { 
 background-image:url(images/v2/SpinRightButton_light_disabled.png); 
}
```

