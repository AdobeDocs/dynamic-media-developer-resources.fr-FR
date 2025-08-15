---
title: Barre de contrôle principale
description: La barre de contrôle principale est la zone rectangulaire sur les ordinateurs de bureau et les tablettes qui contient toutes les commandes de l’interface utilisateur (à l’exception des boutons Grande page) disponibles pour la visionneuse de Search catalogue électronique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cee6a4d4-4099-4bc8-9d67-00a1e963a139
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---

# Barre de contrôle principale{#main-control-bar}

La barre de contrôle principale est la zone rectangulaire sur les ordinateurs de bureau et les tablettes qui contient toutes les commandes de l’interface utilisateur (à l’exception des boutons Grande page) disponibles pour la visionneuse de Search catalogue électronique.

Sur les téléphones mobiles, il conserve toujours les vignettes, la table des matières, les boutons Télécharger, Imprimer, Favoris, Social partager, plein écran et Fermer. Toutefois, les boutons Première page et Dernière page, ainsi que l’indicateur de page sont supprimés de la barre de contrôle principale et ajoutés à la barre de contrôle secondaire à la place. Par défaut, la barre de contrôle principale est affichée en haut de la zone de la visionneuse sur les systèmes de bureau et les téléphones mobiles, et déplacée vers le bas de la zone de la visionneuse sur les tablettes. Prend toujours toute la largeur disponible de la visionneuse. Il est possible de modifier sa couleur, sa hauteur et sa position verticale dans le CSS par rapport au conteneur de la visionneuse.

L’apparence de la barre de contrôle principale est contrôlée par le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p>Position depuis le haut de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p>Position depuis le bas de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de contrôle principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de contrôle principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** : pour configurer une barre de contrôle principale grise de 36 pixels de haut et positionnée en haut du conteneur de la visionneuse.

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

La barre de contrôle principale prend en charge une fonction de défilement en option. Il est activé si la largeur de la visionneuse est trop petite et qu’il n’y a pas assez d’espace pour tenir tous les boutons prédéfinis dans la barre de contrôle. Dans ce cas, un bouton fléché à deux états apparaît dans la partie droite de la barre de contrôle. Cliquez ou appuyez sur ce bouton pour faire défiler tous les éléments de la barre de contrôle vers la gauche ou vers la droite, selon l’état du bouton de défilement. Le principal cas d’utilisation de cette fonctionnalité concerne les appareils mobiles avec de petits écrans en orientation portrait.

La fonction de défilement est activée pour la barre de contrôle principale et est désactivée pour la barre de contrôle secondaire. La fonctionnalité est activée et désactivée à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

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
   <td colname="col2"> <p>Lorsque cette option est définie sur <span class="codeph"> statique </span> , la fonction de défilement est désactivée. </p> <p>Définissez cette propriété sur <span class="codeph"> absolute </span> pour activer la fonction de défilement. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le bouton de défilement est ajouté à un élément conteneur spécial qui positionne correctement le bouton. Il vous permet de mettre en forme la zone autour du bouton différemment du reste de l’arrière-plan de la barre de contrôle au cas où la hauteur du bouton de défilement serait inférieure à la hauteur de la barre de contrôle.

L’apparence de ce conteneur de boutons de défilement est contrôlée par le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Normalement, doit être égale ou supérieure à la largeur du bouton de défilement lui-même. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du conteneur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez dimensionner et appliquer une enveloppe au bouton de défilement lui-même au moyen de CSS.

L’aspect de ce bouton est contrôlé par le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
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
   <td colname="col2"> <p>Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge les sélecteurs d’attributs `state` et `selected` , qui peuvent être utilisés pour appliquer différents habillages à différents états de bouton. En particulier, `state="selected"` correspond à l’état initial du bouton de défilement lorsqu’il est possible de faire défiler le contenu de la barre de contrôle vers la gauche. Le `state="default"` correspond à l’état dans lequel le contenu est défilé complètement vers la gauche et le bouton de défilement suggère de le ramener à l’état initial.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

**Exemple** - Pour activer la fonction de défilement dans la barre de commande principale pour les téléphones mobiles. Et, configurez un bouton de défilement de 64 x 64 pixels qui affiche une image différente pour chacun des 4 états de bouton différents lorsqu’il est sélectionné ou non sélectionné :

```
.s7ecatalogsearchviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```
