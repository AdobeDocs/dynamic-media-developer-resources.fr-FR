---
title: PageView.doubleclick
description: PageView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d53a8723-d710-4722-b1a7-c88d3b9d270b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de double-clic/appui sur pour zoomer. Si vous définissez sur <span class="codeph"> aucun </span>, double-cliquez/appuyez sur le zoom. S’il est défini sur <span class="codeph"> zoom </span> que vous cliquez sur l’image effectue un zoom avant d’une étape de zoom ; Ctrl+Clic effectue un zoom arrière d’une étape de zoom avant. Si vous définissez sur <span class="codeph"> réinitialisation </span>, un seul clic sur l’image réinitialise le zoom au niveau de zoom initial. Pour <span class="codeph"> paramètre zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est égal ou supérieur à la limite spécifiée, sinon le zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Facultatif.

## Par défaut {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` sur les ordinateurs de bureau ; `zoomReset` sur les appareils tactiles.

## Exemple {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
