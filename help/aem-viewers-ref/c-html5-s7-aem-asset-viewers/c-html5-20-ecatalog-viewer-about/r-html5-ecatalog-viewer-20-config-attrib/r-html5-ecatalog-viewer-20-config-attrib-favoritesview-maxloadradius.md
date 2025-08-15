---
title: FavoritesView.maxloadradius
description: FavoritesView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 6bbf75f1-96e7-496d-9f5c-6f449f76bfdd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 5%

---

# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

` [FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Spécifie le comportement de préchargement du composant. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> -1</span>, toutes les vignettes sont chargées simultanément lorsque le composant est initialisé ou que la ressource est modifiée. </p> <p>Lorsque la valeur est 0<span class="codeph"></span>, seules les vignettes visibles sont chargées. </p> <p> Lorsque cette option est définie sur <span class="codeph"><span class="varname"> preloadnbr</span></span>, vous pouvez spécifier combien de lignes invisibles autour de la zone visible sont préchargées. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`1`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`maxloadradius=0`
