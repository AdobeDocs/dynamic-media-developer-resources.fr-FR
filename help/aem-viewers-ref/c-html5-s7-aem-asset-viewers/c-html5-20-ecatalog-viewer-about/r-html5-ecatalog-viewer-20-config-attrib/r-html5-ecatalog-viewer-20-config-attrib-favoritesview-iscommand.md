---
description: Chaîne de commande de diffusion d’images appliquée à toutes les miniatures.
seo-description: Chaîne de commande de diffusion d’images appliquée à toutes les miniatures.
seo-title: FavorisView.iscommand
solution: Experience Manager
title: FavorisView.iscommand
topic: Dynamic media
uuid: 59a25b65-a08f-46e9-a9eb-33672e4a0cb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavorisView.iscommand{#favoritesview-iscommand}

Chaîne de commande de diffusion d’images appliquée à toutes les miniatures.

` [FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Si elle est spécifiée dans l'URL, toutes les occurrences de <span class="codeph"> &amp;</span> et <span class="codeph"> =</span> doivent être codées en HTTP comme <span class="codeph"> %26</span> et <span class="codeph"> %3D, respectivement.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

Aucune

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Lorsqu’elle est spécifiée dans l’URL de la visionneuse.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsqu’elle est spécifiée dans les données de configuration.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
