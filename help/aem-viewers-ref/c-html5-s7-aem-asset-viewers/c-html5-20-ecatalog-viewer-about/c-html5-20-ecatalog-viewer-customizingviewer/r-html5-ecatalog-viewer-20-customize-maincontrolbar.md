---
description: La barre de contrôle principale est la zone rectangulaire des ordinateurs de bureau et des tablettes qui contiennent tous les contrôles de l’interface utilisateur (à l’exception des boutons Grande page) disponibles pour la visionneuse de catalogue électronique.
solution: Experience Manager
title: Barre de contrôle principale
feature: Dynamic Media Classic,Visionneuses,SDK/API,eCatalog
role: Developer,User
exl-id: 4db16599-ede0-47ae-bb5a-840655d3620b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 1%

---

# Barre de contrôle principale{#main-control-bar}

La barre de contrôle principale est la zone rectangulaire des ordinateurs de bureau et des tablettes qui contiennent tous les contrôles de l’interface utilisateur (à l’exception des boutons Grande page) disponibles pour la visionneuse de catalogue électronique.

Sur les téléphones mobiles, il conserve toujours les boutons Miniatures, Table des matières, Télécharger, Imprimer, Favoris, Partage sur les réseaux sociaux, Plein écran et Fermer. Toutefois, les boutons Première page et Dernière page et Indicateur de page sont supprimés de la barre de contrôle principale et ajoutés à la barre de contrôle secondaire à la place. Par défaut, la barre de contrôle principale s’affiche en haut de la zone de la visionneuse sur les ordinateurs de bureau et les téléphones mobiles, et est déplacée vers le bas de la zone de visionneuse sur les tablettes. Elle prend toujours la largeur totale de la visionneuse disponible. Il est possible de modifier sa couleur, sa hauteur et sa position verticale dans le CSS, par rapport au conteneur de la visionneuse.

L’aspect de la barre de contrôle principale est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position à partir du haut de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Position à partir du bas de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de contrôle principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de contrôle principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**  : pour configurer une barre de contrôle principale grise de 36 pixels et positionnée en haut du conteneur de la visionneuse.

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

La barre de contrôle principale prend en charge une fonction de défilement facultative. Cette option est activée si la largeur de la visionneuse est trop petite et qu’il n’y a pas assez d’espace pour que tous les boutons prédéfinis de la barre de contrôle s’adaptent. Dans ce cas, une flèche à deux états s’affiche dans la partie droite de la barre de contrôle. Cliquez ou appuyez sur ce bouton pour faire défiler tous les éléments de la barre de contrôle vers la gauche ou vers la droite, selon l’état du bouton de défilement. Les Principaux cas d’utilisation de cette fonctionnalité sont les appareils mobiles avec de petits écrans en orientation portrait.

La fonction de défilement est activée pour la barre de contrôle principale et désactivée pour la barre de contrôle secondaire. La fonctionnalité est activée et désactivée à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position </span> </p> </td> 
   <td colname="col2"> <p>Lorsqu’elle est définie sur <span class="codeph"> statique </span>, la fonction de défilement est désactivée. </p> <p>Définissez cette propriété sur <span class="codeph"> absolu </span> pour activer la fonction de défilement. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton de défilement est ajouté à un élément de conteneur spécial qui positionne correctement le bouton et permet de mettre en forme la zone autour du bouton différemment du reste de l’arrière-plan de la barre de contrôle, au cas où la hauteur du bouton de défilement serait inférieure à la hauteur de la barre de contrôle.

L’aspect de ce conteneur de boutons de défilement est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Normalement, doit être égal ou supérieur à la largeur du bouton de défilement lui-même. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du conteneur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez dimensionner et appliquer un habillage au bouton de défilement lui-même au moyen d’une feuille CSS.

L’aspect de ce bouton est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p>Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge les sélecteurs d’attributs `state` et `selected`, qui peuvent être utilisés pour appliquer différents habillages à différents états de bouton. En particulier, `state="selected"` correspond à l’état initial du bouton de défilement lorsqu’il est possible de faire défiler le contenu de la barre de contrôle vers la gauche ; `state="default"` correspond à l’état lorsque le contenu est défilé jusqu’à la gauche et que le bouton de défilement suggère de le renvoyer à l’état initial.

L’info-bulle de bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

**Exemple**  : pour activer la fonction de défilement dans la barre de contrôle principale pour les téléphones mobiles, configurez un bouton de défilement de 64 x 64 pixels qui affiche une image différente pour chacun des 4 états de bouton différents lorsqu’il est sélectionné ou non :

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
