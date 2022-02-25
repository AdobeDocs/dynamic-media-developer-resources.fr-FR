---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ded8168e-08f7-4bc0-bb8a-624bac82759e
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`step`*[, *`limit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> step</span> </span> </p> </td> 
   <td colname="col2"> <p> Configure le nombre d’actions de zoom avant et arrière requises pour augmenter ou réduire la résolution d’un facteur de deux. La modification de résolution pour chaque action de zoom est de 2^1 par étape. Définissez sur . <span class="codeph"> 0</span> pour effectuer un zoom en pleine résolution avec une seule action de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> limit</span> </span> </p> </td> 
   <td colname="col2"> <p> Indique la résolution maximale du zoom, par rapport à l’image à résolution complète. La valeur par défaut est <span class="codeph"> 1,0</span>, qui n’autorise pas le zoom au-delà de la résolution totale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-50bcd15223174bb79ce08b31ea03d682}

Facultatif.

## Par défaut {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## Exemple {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
