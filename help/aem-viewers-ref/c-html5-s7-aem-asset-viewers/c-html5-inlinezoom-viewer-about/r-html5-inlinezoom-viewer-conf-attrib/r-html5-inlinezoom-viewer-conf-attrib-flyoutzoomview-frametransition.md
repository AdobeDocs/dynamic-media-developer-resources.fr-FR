---
title: FlyoutZoomView.frametransition
description: FlyoutZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 39cb629a-3940-4206-91cd-fe9a9f4d9f75
TQID: 'https://experienceleague.adobe.com/AX55D86n9ifbW-nRBlNZUW6WyTxVlGf5jlfTr6owRE4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 6%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`durée`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aucun|fondu</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> Spécifie le type de l'effet appliqué à la vue principale lors de la modification des ressources. </p> <p><span class="codeph"> aucun</span> signifie aucune transition, le changement de vue principale se produit instantanément. </p> <p><span class="codeph"> fondu</span> active la transition de fondu enchaîné où l’ancienne image est fondue et la nouvelle image est fondue </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p> Nombre de secondes nécessaires à l'animation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

Aucune

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1`
