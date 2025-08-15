---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aucun|zoom|réinitialisation|réinitialisationZoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions d’un simple clic/appuyer sur le zoom. La définition sur <span class="codeph"> aucun </span> désactive le zoom d’un clic/appuyer unique. S’il est configuré pour <span class="codeph"> tourner </span> , cliquer sur l’image effectue un zoom d’un pas de zoom ; CTRL+clic effectue un zoom arrière d’un pas de zoom. Le paramètre de <span class="codeph"> réinitialisation </span> provoque un simple clic sur l’image pour réinitialiser le zoom au niveau de rotation initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est égal ou supérieur à la limite spécifiée, sinon le zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` Sur les ordinateurs de bureau ; `none` sur les appareils tactiles.

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
