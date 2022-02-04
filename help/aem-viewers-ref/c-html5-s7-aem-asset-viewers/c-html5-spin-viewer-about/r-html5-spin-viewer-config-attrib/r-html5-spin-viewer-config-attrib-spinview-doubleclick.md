---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage de double-clic/clic pour les actions de rotation. Définir sur <span class="codeph"> none </span> désactive la rotation double-clic/appuyez sur . Si la variable est définie sur <span class="codeph"> zoom </span>, cliquer sur la rotation de l’image en une seule étape de rotation ; Ctrl+Clic trace une étape de rotation. Définir sur <span class="codeph"> reset </span> fait qu’un seul clic sur l’image réinitialise la rotation au niveau de rotation initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de rotation actuel est à la limite spécifiée ou au-delà de cette limite ; dans le cas contraire, une rotation est appliquée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`reset` sur les ordinateurs de bureau ; `zoomReset` sur les périphériques tactiles.

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
