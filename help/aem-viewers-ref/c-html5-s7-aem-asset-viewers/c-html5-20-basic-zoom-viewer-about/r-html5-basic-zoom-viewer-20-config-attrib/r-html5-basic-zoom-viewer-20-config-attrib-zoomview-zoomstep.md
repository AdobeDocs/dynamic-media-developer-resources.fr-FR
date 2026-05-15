---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ded8168e-08f7-4bc0-bb8a-624bac82759e
TQID: 'https://experienceleague.adobe.com/hJGTnjDC-x9P3Q0vbq0mXuumwtZHAVfxcVWPXkemyoI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`step`*[, *`limit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> étape </span> </span> </p> </td> 
   <td colname="col2"> <p> Configure le nombre d’actions de zoom avant et de zoom arrière requises pour augmenter ou réduire la résolution d’un facteur deux. La modification de la résolution pour chaque action de zoom est de 2^1 par étape. Définissez sur <span class="codeph"> 0</span> pour effectuer un zoom à résolution complète avec une seule action de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> limite </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique la résolution de zoom maximale par rapport à l’image en résolution complète. La valeur par défaut est <span class="codeph"> 1,0</span>, ce qui n’autorise pas le zoom au-delà de la résolution complète. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-50bcd15223174bb79ce08b31ea03d682}

Facultatif.

## Par défaut {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## Exemple {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
