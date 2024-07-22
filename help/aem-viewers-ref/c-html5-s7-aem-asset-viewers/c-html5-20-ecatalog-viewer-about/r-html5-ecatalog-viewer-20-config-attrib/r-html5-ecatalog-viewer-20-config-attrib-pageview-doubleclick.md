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
   <td colname="col2"> <p> Configure le mappage des actions de zoom en double-cliquant/appuyant. La définition de sur <span class="codeph"> none </span> désactive le zoom double-clic/appuyez sur . Si vous définissez sur <span class="codeph"> zoom </span>, cliquez sur l’image pour effectuer un zoom avant sur une étape de zoom ; Ctrl+Clic fait un zoom arrière sur une étape de zoom. La définition de la valeur <span class="codeph"> reset </span> entraîne un seul clic sur l’image pour réinitialiser le zoom sur le niveau de zoom initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est à ou au-delà de la limite spécifiée, sinon un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Facultatif.

## Par défaut {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` sur les ordinateurs de bureau ; `zoomReset` sur les appareils tactiles.

## Exemple {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
