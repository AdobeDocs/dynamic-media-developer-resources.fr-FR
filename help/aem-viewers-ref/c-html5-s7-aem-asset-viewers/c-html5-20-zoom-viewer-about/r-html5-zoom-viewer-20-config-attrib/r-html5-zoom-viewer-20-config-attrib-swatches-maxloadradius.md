---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom
role: Developer,User
exl-id: df9d5be4-d1e1-4b72-a7e7-0f3611278d2a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Indique le comportement de préchargement du composant. Lorsqu’elle est définie sur <span class="codeph"> -1</span>, tous les échantillons sont chargés simultanément lorsque le composant est initialisé ou que la ressource est modifiée. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> 0</span>, seuls les échantillons visibles sont chargés. </p> <p><span class="codeph"><span class="varname"> </span></span> preloadnbrdéfinit le nombre de lignes/colonnes invisibles autour de la zone visible qui sont préchargées. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=-1`
