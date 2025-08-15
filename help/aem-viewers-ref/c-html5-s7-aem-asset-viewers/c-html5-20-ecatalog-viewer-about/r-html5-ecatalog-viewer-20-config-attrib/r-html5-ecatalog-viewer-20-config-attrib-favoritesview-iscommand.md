---
title: FavoritesView.iscommand
description: Chaîne de commande du service d’images appliquée à toutes les miniatures.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 1b6198f4-367d-437a-b8b1-206519567af0
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# FavoritesView.iscommand{#favoritesview-iscommand}

Chaîne de commande du service d’images appliquée à toutes les miniatures.

` [FavoritesView.|<containerId>_favoritesView.]iscommand= *`Commande isCommand`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Commande isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Si elles sont spécifiées dans l’URL, toutes les occurrences de <span class="codeph"> &amp;</span> et =<span class="codeph"> </span> doivent être codées en HTTP en tant que <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

Aucune

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Lorsque cela est spécifié dans l’URL de la visionneuse.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsque cela est spécifié dans les données de configuration.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
