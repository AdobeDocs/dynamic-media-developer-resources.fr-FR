---
description: 'null'
seo-description: 'null'
seo-title: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
topic: Dynamic media
uuid: c62302b0-d034-49d4-b5a8-1a77a46fe889
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des -clic/clic sur le pour effectuer un zoom sur les actions. La valeur <span class="codeph"> Aucune </span> désactive le zoom par clic/clic sur le. Si elle est définie pour <span class="codeph"> effectuer un zoom </span> en cliquant sur l’image, la fonction effectue un zoom avant sur une étape de zoom ; CTRL+clic permet d’effectuer un zoom arrière sur une étape de zoom. Si vous <span class="codeph"> réinitialisez </span> , un seul clic sur l’image réinitialise le zoom au niveau de zoom initial. Dans le cas de <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est supérieur ou égal à la limite spécifiée, sinon un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Facultatif.

## Par défaut {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] sur les ordinateurs de bureau; [!DNL `zoomReset`] sur les périphériques tactiles.

## Exemple {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
