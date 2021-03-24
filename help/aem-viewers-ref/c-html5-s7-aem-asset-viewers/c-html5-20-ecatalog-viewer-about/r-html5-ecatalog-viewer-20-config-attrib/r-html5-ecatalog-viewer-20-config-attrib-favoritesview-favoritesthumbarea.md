---
description: FavoritesView.favoritesThumbView
solution: Experience Manager
title: FavoritesView.favoritesThumbView
feature: Dynamic Media Classic, Visionneuses, SDK/API, Catalogue électronique
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 9%

---


# FavoritesView.favoritesThumbView{#favoritesview-favoritesthumbview}

` [FavoritesView.|<containerId>_favoritesView.]favoritesThumbArea= *`zone`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> zone</span></span> </p> </td> 
   <td colname="col2"> <p> Indique la zone de recadrage de la miniature Favoris. Exprimé en tant que valeur relative par rapport à la taille totale de l’image, avec une plage allant de <span class="codeph"> 0</span> à <span class="codeph"> 1.0</span>. </p> <p>La valeur <span class="codeph"> 1</span> signifie que l’image image entière est utilisée pour la miniature. </p> <p>La valeur <span class="codeph"> 0.1</span> signifie que seulement 10 % de la taille de l’image est utilisée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`0.1`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`favoritesThumbArea=0.5`
