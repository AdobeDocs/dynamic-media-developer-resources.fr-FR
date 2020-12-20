---
description: 'null'
seo-description: 'null'
seo-title: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
topic: Dynamic media
uuid: e72ae5d6-574e-4f30-827c-021ce5dafcee
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 10%

---


# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

[!DNL `[ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

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

[!DNL `1`]

## Exemple {#section-472614b59e04430490a7f16c932bce89}

[!DNL `maxloadradius=0`]
