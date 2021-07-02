---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: fd432573-677f-4c46-9cc1-88089496ce75
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> Permet ou désactive la possibilité pour un utilisateur de faire défiler les échantillons avec la souris ou à l’aide de mouvements tactiles. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> Fonctions comprises dans la plage <span class="codeph"> 0-1 </span>. Il s’agit d’une valeur <span class="codeph"> % </span> pour le mouvement dans la mauvaise direction de la vitesse réelle. Si elle est définie sur <span class="codeph"> 1 </span>, elle se déplace avec la souris. S’il est défini sur <span class="codeph"> 0 </span>, il ne vous permet pas du tout de vous diriger dans la mauvaise direction. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,0.5`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enabledragging=0`
