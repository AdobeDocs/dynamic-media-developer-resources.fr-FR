---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0fcc1f5c-a735-430d-be0c-c00ed08830df
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` sur les ordinateurs de bureau ; `none` sur les appareils tactiles.

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
