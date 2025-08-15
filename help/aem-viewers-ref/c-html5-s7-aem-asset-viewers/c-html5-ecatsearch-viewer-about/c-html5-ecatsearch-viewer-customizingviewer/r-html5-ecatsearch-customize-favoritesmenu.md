---
title: Menu Favoris
description: La liste déroulante du menu Favoris s’affiche dans la barre de contrôle. Il se compose d’un bouton et d’un panneau qui se développe lorsqu’un utilisateur clique ou appuie sur un bouton. Le panneau contient des outils Favoris individuels.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 129a8451-f634-44ad-adb1-f30d2621cb29
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# Menu Favoris{#favorites-menu}

La liste déroulante du menu Favoris s’affiche dans la barre de contrôle. Il se compose d’un bouton et d’un panneau qui se développe lorsqu’un utilisateur clique ou appuie sur un bouton. Le panneau contient des outils Favoris individuels.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La position et la taille du menu Favoris dans l’interface utilisateur de la visionneuse sont contrôlées par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoritesmenu
```

**Propriétés CSS du bouton de menu Favoris**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge haut </span> </p> </td> 
   <td colname="col2"> <p> Décalage par rapport au haut de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge gauche </span> </p> </td> 
   <td colname="col2"> <p> Distance jusqu’au bouton suivant à gauche ou à gauche de la barre de contrôle si ce bouton est le premier d’une rangée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - configurez un menu Favoris positionné à quatre pixels du haut de la barre de contrôle et à dix pixels du bouton le plus proche à gauche et d’une taille de 28 x 28 pixels.

```
.s7ecatalogsearchviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

L’apparence du bouton de menu Favoris est contrôlée par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton
```

**Propriétés CSS du bouton Favoris**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état donné du bouton. </p> </td> 
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

Exemple - configurez un bouton de menu Favoris qui affiche une image différente pour chacun des quatre états de bouton différents.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

L’aspect du panneau qui contient des icônes Favoris individuelles est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel
```

**Propriétés CSS du panneau de menu Favoris**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - configurez un panneau pour obtenir une couleur transparente.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```
