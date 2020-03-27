---
description: La barre de contrôle principale est la zone rectangulaire sur les ordinateurs de bureau et les tablettes qui contient tous les contrôles de l’interface utilisateur (à l’exception des boutons Grande page) disponibles pour la visionneuse de catalogue électronique.
seo-description: La barre de contrôle principale est la zone rectangulaire sur les ordinateurs de bureau et les tablettes qui contient tous les contrôles de l’interface utilisateur (à l’exception des boutons Grande page) disponibles pour la visionneuse de catalogue électronique.
seo-title: Barre de contrôle principale
solution: Experience Manager
title: Barre de contrôle principale
topic: Dynamic media
uuid: 0900f678-d7ec-4653-bc8a-21b8da7d5044
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Barre de contrôle principale{#main-control-bar}

La barre de contrôle principale est la zone rectangulaire sur les ordinateurs de bureau et les tablettes qui contient tous les contrôles de l’interface utilisateur (à l’exception des boutons Grande page) disponibles pour la visionneuse de catalogue électronique.

Sur les téléphones mobiles, il conserve toujours les boutons Miniatures, Table des matières, Télécharger, Imprimer, Favoris, Partage sur les réseaux sociaux, Plein écran et Fermer. Toutefois, les boutons Première page et Dernière page et Indicateur de page sont supprimés de la barre de contrôle principale et ajoutés à la barre de contrôle secondaire. Par défaut, la barre de contrôle principale s’affiche dans la partie supérieure de la zone du lecteur sur les ordinateurs de bureau et les téléphones mobiles, puis est déplacée dans la partie inférieure de la zone du lecteur sur les tablettes. Il prend toujours la largeur totale de la visionneuse disponible. Il est possible de modifier sa couleur, sa hauteur et sa position verticale dans la page CSS, par rapport au  de la visionneuse.

L’aspect de la barre de contrôle principale est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position en haut du lecteur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Position à partir du bas du lecteur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de contrôle principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de contrôle principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** : pour configurer une barre de contrôle principale grise de 36 pixels et positionnée en haut du  de la visionneuse.

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

La barre de contrôle principale prend en charge une fonction de défilement facultative. Elle est activée si la largeur de la visionneuse est trop petite et si l’espace disponible ne permet pas d’ajuster tous les boutons prédéfinis dans la barre de contrôle. Dans ce cas, un bouton de flèche à deux états s’affiche sur le côté droit de la barre de contrôle. Cliquez ou appuyez sur ce bouton pour faire défiler tous les éléments de la barre de contrôle vers la gauche ou vers la droite, selon l’état du bouton de défilement. Le principal cas d’utilisation de cette fonctionnalité sont les périphériques mobiles avec de petits écrans en orientation portrait.

La fonction de défilement est activée pour la barre de contrôle principale et désactivée pour la barre de contrôle secondaire. La fonction est activée et désactivée à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position </span> </p> </td> 
   <td colname="col2"> <p>Lorsqu’elle est définie sur <span class="codeph"> statique </span> , la fonction de défilement est désactivée. </p> <p>Définissez cette propriété sur <span class="codeph"> absolu </span> pour activer la fonction de défilement. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton de défilement est ajouté à un élément  spécial qui positionne correctement le bouton et vous permet de mettre en forme la zone entourant le bouton différemment du reste de l’arrière-plan de la barre de contrôle si la hauteur du bouton de défilement est inférieure à la hauteur de la barre de contrôle.

L’aspect de ce de bouton de défilement est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Normalement, cette valeur doit être égale ou supérieure à la largeur du bouton de défilement lui-même. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan . </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez dimensionner et habiller le bouton de défilement lui-même au moyen de CSS.

L’aspect de ce bouton est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
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
   <td colname="col2"> <p>Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge les sélecteurs `state` et `selected` d’attributs, qui peuvent être utilisés pour appliquer différents habillages à différents états de bouton. Correspond en particulier à l’état initial du bouton de défilement lorsqu’il est possible de faire défiler le contenu de la barre de contrôle vers la gauche ; `state="selected"` `state="default"` correspond à l’état lorsque le contenu est fait défiler jusqu’à la gauche et que le bouton de défilement suggère de le rétablir.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

**Exemple** : pour activer la fonction de défilement dans la barre de contrôle principale pour les téléphones mobiles, et pour configurer un bouton de défilement de 64 x 64 pixels qui affiche une image différente pour chacun des 4 états de bouton différents lorsqu’il est sélectionné ou non :

```
.s7ecatalogviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```

