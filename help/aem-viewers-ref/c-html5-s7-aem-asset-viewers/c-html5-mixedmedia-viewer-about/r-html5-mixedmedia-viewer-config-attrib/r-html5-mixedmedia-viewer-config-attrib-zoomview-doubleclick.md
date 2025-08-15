---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e87981f8-8174-432a-89ea-fae74d0584ad
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aucun|zoom|réinitialisation|réinitialisationZoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de double-clic/appui vers les actions de zoom. La définition sur <span class="codeph"> aucun </span> désactive le double-clic/appuyer sur le zoom. Si vous souhaitez <span class="codeph"> zoomer </span> , cliquer sur l’image effectue un zoom d’un pas de zoom. CTRL+clic effectue un zoom arrière d’un pas de zoom. Le paramètre de <span class="codeph"> réinitialisation </span> provoque un simple clic sur l’image pour réinitialiser le zoom au niveau de zoom initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est égal ou supérieur à la limite spécifiée, sinon le zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` Sur les ordinateurs de bureau ; `zoomReset` sur les appareils tactiles.

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
