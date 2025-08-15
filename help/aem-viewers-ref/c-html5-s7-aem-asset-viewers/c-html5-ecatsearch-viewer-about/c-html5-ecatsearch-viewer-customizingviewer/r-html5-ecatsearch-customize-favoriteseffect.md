---
title: Effet Favoris
description: La visionneuse affiche les icônes de Favoris sur la vue principale à l’endroit où elle a été ajoutée par l’utilisateur.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 7603c873-a2d1-4a24-85a6-8e56a1f207de
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Effet Favoris{#favorites-effect}

La visionneuse affiche les icônes de Favoris sur la vue principale à l’endroit où elle a été ajoutée par l’utilisateur.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect de l’icône des Favoris est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon
```

**Propriétés CSS de l’icône Favori**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Image affichée pour l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Configurez une icône Favoris de 36 x 36 pixels.

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Sur les systèmes de bureau, le composant prend en charge le sélecteur d’attributs `cursortype` que vous pouvez appliquer à la classe `.s7favoriteseffect` et contrôle le type du curseur en fonction de l’action de l’utilisateur sélectionné. Les valeurs `cursortype` suivantes sont prises en charge :

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>L’utilisateur affiché ajoute une nouvelle icône Favoris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>L’utilisateur affiché supprime une icône de favoris existante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view </span> </p> </td> 
   <td colname="col2"> <p>Affiché en mode de fonctionnement normal lorsque la modification des Favoris n’est pas active. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : utilisez différents curseurs de souris pour chaque type d’état du composant.

```
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```
