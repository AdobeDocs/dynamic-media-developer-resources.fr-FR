---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fd432573-677f-4c46-9cc1-88089496ce75
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Permet ou désactive la possibilité pour un utilisateur de faire défiler les échantillons avec la souris ou à l’aide de mouvements tactiles. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Fonctions comprises dans la plage <span class="codeph"> 0-1 </span>. Il s’agit d’une valeur <span class="codeph"> % </span> pour le mouvement dans la mauvaise direction de la vitesse réelle. Si elle est définie sur <span class="codeph"> 1 </span>, elle se déplace avec la souris. Si elle est définie sur <span class="codeph"> 0 </span>, elle ne vous permet pas du tout de vous diriger dans la mauvaise direction. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,0.5`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enabledragging=0`
