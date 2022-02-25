---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c2292b5b-5b4e-4368-9495-9108042ec2f1
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de zoom d’un simple clic/d’un simple clic. Définir sur <span class="codeph"> none </span> désactive le zoom en un clic/en un clic. Si la variable est définie sur <span class="codeph"> zoom </span> le fait de cliquer sur l’image agrandit une étape de zoom ; CTRL+Clic permet d’afficher un zoom arrière sur une étape de zoom. Définir sur <span class="codeph"> reset </span> fait qu’un seul clic sur l’image réinitialise le zoom sur le niveau de zoom initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel se situe à la limite spécifiée ou au-delà de cette dernière ; dans le cas contraire, un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-50bcd15223174bb79ce08b31ea03d682}

Facultatif.

## Par défaut {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` Sur les ordinateurs de bureau ; `none` sur les périphériques tactiles.

## Exemple {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
