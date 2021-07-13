---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom
role: Developer,User
exl-id: 9f52542e-398c-45a2-89ea-95c9aefbde3e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de zoom en double-cliquant/appuyant. La définition de sur <span class="codeph"> none </span> désactive le double-clic/l’appui sur le zoom. Si la valeur est <span class="codeph"> zoom </span>, cliquez sur l’image pour effectuer un zoom avant sur une étape de zoom ; CTRL+Clic permet d’afficher un zoom arrière sur une étape de zoom. Si vous définissez cette valeur sur <span class="codeph"> et réinitialiser </span>, un seul clic sur l’image réinitialise le zoom au niveau de zoom initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est à la limite spécifiée ou au-delà de cette dernière, sinon un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`reset` sur les ordinateurs de bureau ;  `zoomReset` sur les périphériques tactiles.

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
