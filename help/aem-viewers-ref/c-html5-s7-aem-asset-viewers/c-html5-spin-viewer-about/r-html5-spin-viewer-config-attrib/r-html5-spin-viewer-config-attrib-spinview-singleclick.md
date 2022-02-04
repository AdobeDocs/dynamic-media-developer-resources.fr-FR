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
ht-degree: 4%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de zoom d’un simple clic/d’un simple clic. Définir sur <span class="codeph"> none </span> désactive le zoom en un clic/en un clic. Si la variable est définie sur <span class="codeph"> rotation </span> le fait de cliquer sur l’image agrandit une étape de zoom ; CTRL+Clic permet d’afficher un zoom arrière sur une étape de zoom. Définir sur <span class="codeph"> reset </span> fait qu’un seul clic sur l’image réinitialise le zoom sur le niveau de rotation initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel se situe à la limite spécifiée ou au-delà de cette dernière ; dans le cas contraire, un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` Sur les ordinateurs de bureau ; `none` sur les périphériques tactiles.

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
