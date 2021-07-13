---
description: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses à 360°
role: Developer,User
exl-id: 919477d0-87d9-4cf7-a7c8-0fbb68c6ff96
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 6%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> étape</span></span> </p> </td> 
   <td colname="col2"> <p> Configure le nombre d’actions de zoom avant et arrière requises pour augmenter ou réduire la résolution d’un facteur de deux. La modification de résolution pour chaque action de zoom est de 2^1 par étape. Définissez cette variable sur <span class="codeph"> 0</span> pour effectuer un zoom en pleine résolution avec une seule action de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limiter</span></span> </p> </td> 
   <td colname="col2"> <p> Indique la résolution maximale du zoom, par rapport à l’image à résolution complète. La valeur par défaut est <span class="codeph"> 1.0</span>, ce qui n’autorise pas le zoom au-delà de la résolution totale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
