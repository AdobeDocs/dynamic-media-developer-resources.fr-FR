---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
topic: Dynamic Media
uuid: 13ea3917-346a-47c3-a535-f771910fa1c3
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 7%

---


# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Indique le comportement de préchargement du composant. </p> <p>Lorsqu’elles sont définies sur <span class="codeph"> -1</span>, les miniatures sont chargées simultanément lorsque le composant est initialisé ou que la ressource change. </p> <p>Lorsque cette valeur est définie sur <span class="codeph"> 0</span>, seules les vignettes visibles sont chargées. </p> <p>Le paramètre <span class="codeph"><span class="varname"> preloadnbr</span></span> définit le nombre de lignes/colonnes invisibles autour de la zone visible qui sont préchargées. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-a3abd04c03e14c238a07349ce50d8310}

Facultatif.

## Par défaut {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## Exemple {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`
