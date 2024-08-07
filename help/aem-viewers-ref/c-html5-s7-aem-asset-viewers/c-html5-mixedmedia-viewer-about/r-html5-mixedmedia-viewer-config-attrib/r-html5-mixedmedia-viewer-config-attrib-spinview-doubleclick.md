---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage de double-clic/clic pour les actions de rotation. La définition de sur <span class="codeph"> none </span> désactive la rotation double-clic/appui. Si celle-ci est définie sur <span class="codeph"> zoom </span>, cliquez sur la rotation de l’image en une seule étape de rotation ; Ctrl+Clic chevauche une étape de rotation. La définition de la valeur <span class="codeph"> reset </span> entraîne un seul clic sur l’image pour réinitialiser la rotation au niveau de rotation initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de rotation actuel est à ou au-delà de la limite spécifiée, sinon la rotation est appliquée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` Sur ordinateurs de bureau ; `zoomReset` sur appareils tactiles.

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
