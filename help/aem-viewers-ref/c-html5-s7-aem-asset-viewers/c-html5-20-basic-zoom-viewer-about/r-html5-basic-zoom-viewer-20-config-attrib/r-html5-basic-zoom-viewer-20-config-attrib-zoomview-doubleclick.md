---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 38c90d7f-ddbc-4123-b90d-02f9cabd785c
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de zoom en double-cliquant/appuyant. La définition de sur <span class="codeph"> none </span> désactive le zoom double-clic/appuyez sur . Si vous définissez sur <span class="codeph"> zoom </span>, cliquez sur l’image pour effectuer un zoom avant sur une étape de zoom ; Ctrl+Clic fait un zoom arrière sur une étape de zoom. La définition de la valeur <span class="codeph"> reset </span> entraîne un seul clic sur l’image pour réinitialiser le zoom sur le niveau de zoom initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est à ou au-delà de la limite spécifiée, sinon un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-50bcd15223174bb79ce08b31ea03d682}

Facultatif.

## Par défaut {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` Sur ordinateurs de bureau ; `zoomReset` sur appareils tactiles.

## Exemple {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
