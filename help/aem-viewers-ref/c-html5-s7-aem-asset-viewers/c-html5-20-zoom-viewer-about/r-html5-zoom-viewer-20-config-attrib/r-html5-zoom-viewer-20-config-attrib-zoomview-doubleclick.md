---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
topic: Dynamic Media
uuid: 8dabc31c-ec7e-4dc0-b528-4f3f43f46721
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage entre les actions de zoom par clic/clic doublon. La définition de <span class="codeph"> none </span> désactive le zoom par clic/clic sur doublon. Si la valeur <span class="codeph"> zoom </span> est définie, le fait de cliquer sur l’image effectue un zoom avant sur une étape de zoom ; CTRL+clic permet d’effectuer un zoom arrière sur une étape de zoom. Si vous définissez <span class="codeph"> reset </span>, un seul clic sur l’image réinitialise le zoom au niveau de zoom initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est égal ou supérieur à la limite spécifiée, sinon un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`reset` sur les ordinateurs de bureau ;  `zoomReset` sur les périphériques tactiles.

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
