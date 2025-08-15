---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e6baef83-b4a8-4bef-bb13-263f3875030d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

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

[!DNL `reset`] sur les ordinateurs de bureau ; [!DNL `zoomReset`] sur les appareils tactiles.

## Exemple {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
