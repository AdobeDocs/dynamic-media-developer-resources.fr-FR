---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic media
uuid: 3e57e235-7888-4ba2-9c8e-4f568a6caa52
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de zoom d’un simple clic/clic. La valeur <span class="codeph"> Aucune </span> désactive le zoom par clic/clic. Si elle est définie pour <span class="codeph"> effectuer un zoom </span> en cliquant sur l’image, la fonction effectue un zoom avant sur une étape de zoom ; CTRL+clic permet d’effectuer un zoom arrière sur une étape de zoom. Si vous <span class="codeph"> réinitialisez </span> , un seul clic sur l’image réinitialise le zoom au niveau de zoom initial. Dans le cas de <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est supérieur ou égal à la limite spécifiée, sinon un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` sur les ordinateurs de bureau; `none` sur les périphériques tactiles.

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
