---
description: Chaîne de commande de diffusion d’images appliquée à toutes les miniatures.
solution: Experience Manager
title: FavoritesView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 114cc5b7-32b9-4d16-ab93-a66f3ec666e0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# FavoritesView.iscommand{#favoritesview-iscommand}

Chaîne de commande de diffusion d’images appliquée à toutes les miniatures.

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Si spécifié dans l’URL, toutes les occurrences de <span class="codeph"> &amp;</span> et <span class="codeph"> =</span> doivent être codées en HTTP sous la forme respectivement de <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

Aucune

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Lorsqu’il est spécifié dans l’URL de la visionneuse.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

Lorsque spécifié dans les données de configuration.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
