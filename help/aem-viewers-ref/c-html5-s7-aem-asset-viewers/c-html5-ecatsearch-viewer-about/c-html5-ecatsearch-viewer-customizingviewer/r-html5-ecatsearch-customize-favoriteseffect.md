---
title: Effet Favoris
description: La visionneuse affiche les icônes Favoris au-dessus de la vue principale à des endroits où elle a été ajoutée à l’origine par l’utilisateur.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 7603c873-a2d1-4a24-85a6-8e56a1f207de
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# Effet Favoris{#favorites-effect}

La visionneuse affiche les icônes Favoris au-dessus de la vue principale à des endroits où elle a été ajoutée à l’origine par l’utilisateur.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect de l’icône Favori est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon
```

**Propriétés CSS de l’icône Favori**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez une icône Favoris 36 x 36 pixels.

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Sur les systèmes de bureau, le composant prend en charge la variable `cursortype` sélecteur d’attributs que vous pouvez appliquer à la variable `.s7favoriteseffect` et contrôle le type du curseur en fonction de l’action utilisateur sélectionnée. Les éléments suivants `cursortype` sont prises en charge :

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>L’utilisateur affiché ajoute une nouvelle icône Favori. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>L’utilisateur affiché supprime une icône Favori existante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view </span> </p> </td> 
   <td colname="col2"> <p>S’affiche en mode de fonctionnement normal lorsque la modification des Favoris n’est pas principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : utilisez des curseurs de souris différents pour chaque type d’état de composant.

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
