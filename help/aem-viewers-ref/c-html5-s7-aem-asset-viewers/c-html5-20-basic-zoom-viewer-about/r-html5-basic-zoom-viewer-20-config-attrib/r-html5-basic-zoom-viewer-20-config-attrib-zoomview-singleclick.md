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
ht-degree: 3%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aucun|zoom|réinitialisation|réinitialisationZoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions d’un simple clic/appuyer sur le zoom. La définition sur <span class="codeph"> aucun </span> désactive le zoom d’un clic/appuyer unique. Si vous souhaitez <span class="codeph"> zoomer </span> , cliquer sur l’image effectue un zoom d’un pas de zoom. CTRL+clic effectue un zoom arrière d’un pas de zoom. Le paramètre de <span class="codeph"> réinitialisation </span> provoque un simple clic sur l’image pour réinitialiser le zoom au niveau de zoom initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est égal ou supérieur à la limite spécifiée, sinon le zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-50bcd15223174bb79ce08b31ea03d682}

Facultatif.

## Par défaut {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` Sur les ordinateurs de bureau ; `none` sur les appareils tactiles.

## Exemple {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
