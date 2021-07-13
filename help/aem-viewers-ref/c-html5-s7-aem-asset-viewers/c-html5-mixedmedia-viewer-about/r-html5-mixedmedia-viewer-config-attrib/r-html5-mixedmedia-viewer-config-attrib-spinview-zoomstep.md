---
description: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,User
exl-id: afc2018f-b222-4fd5-b9dc-88655793efd4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 6%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_2D7F971D503348B8A9559362A1D9B26D"> 
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

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
