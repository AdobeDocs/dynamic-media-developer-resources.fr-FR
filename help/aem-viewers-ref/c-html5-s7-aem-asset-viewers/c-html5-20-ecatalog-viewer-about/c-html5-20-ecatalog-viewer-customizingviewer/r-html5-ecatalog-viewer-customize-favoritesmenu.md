---
description: La liste déroulante du menu Favoris s’affiche dans la barre de contrôle. Il se compose d’un bouton et d’un panneau qui se développe lorsqu’un utilisateur clique ou appuie sur un bouton. Le panneau contient des outils Favoris individuels.
solution: Experience Manager
title: Menu Favoris
feature: Dynamic Media Classic,Visionneuses,SDK/API,eCatalog
role: Developer,User
exl-id: e3c90320-b6fc-4a43-b75f-d39234b1e73c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# Menu Favoris{#favorites-menu}

La liste déroulante du menu Favoris s’affiche dans la barre de contrôle. Il se compose d’un bouton et d’un panneau qui se développe lorsqu’un utilisateur clique ou appuie sur un bouton. Le panneau contient des outils Favoris individuels.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La position et la taille du menu Favoris dans l’interface utilisateur de la visionneuse sont contrôlées avec le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7favoritesmenu
```

**Propriétés CSS du bouton de menu Favoris**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Décalage par rapport au haut de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Distance du bouton suivant à gauche ou du côté gauche de la barre de contrôle s’il s’agit du premier bouton d’une ligne. </p> </td> 
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

Exemple : configurez un menu Favoris qui est positionné à quatre pixels du haut de la barre de contrôle et à dix pixels du bouton le plus proche à gauche et dimensionné à 28 x 28 pixels.

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

L’aspect du bouton de menu Favoris est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

**Propriétés CSS du bouton Favoris**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle de bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : configurez un bouton de menu Favoris qui affiche une image différente pour chacun des quatre états de bouton différents.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

L’aspect du panneau contenant les icônes Favoris individuelles est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**Propriétés CSS du panneau de menu Favoris**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez un panneau pour obtenir une couleur transparente.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```
