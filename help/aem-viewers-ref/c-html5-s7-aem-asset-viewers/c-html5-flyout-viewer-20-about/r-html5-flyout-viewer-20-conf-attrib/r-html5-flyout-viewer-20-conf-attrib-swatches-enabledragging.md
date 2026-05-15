---
title: Nuanciers.enabledragging
description: Nuanciers.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7ffdc886-5631-429f-84b4-4b32b715713d
TQID: 'https://experienceleague.adobe.com/HgxhPRCNG-uZwM9LqggoxuVmyTJhjjB2N3KdmtPSGJk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 6%

---

# Nuanciers.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Active ou désactive la possibilité, pour un utilisateur, de faire défiler les échantillons à l’aide de la souris ou d’un toucher </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Fonctions comprises dans la plage de </span> 0-1 <span class="codeph">. Il s'agit d'une valeur </span> de <span class="codeph"> % pour un mouvement dans le mauvais sens de la vitesse réelle. S’il est défini sur <span class="codeph"> 1 </span>, il se déplace avec la souris. S’il est défini sur <span class="codeph"> 0 </span>, il ne vous permet pas du tout d’avancer dans la mauvaise direction. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0`
