---
description: 'null'
seo-description: 'null'
seo-title: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
topic: Dynamic media
uuid: b08b605e-5ffc-42cc-931d-d67750a8dca8
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de zoom d’un simple clic/clic. La valeur <span class="codeph"> Aucune </span> désactive le zoom par clic/clic. Si elle est définie pour <span class="codeph"> effectuer un zoom </span> en cliquant sur l’image, la fonction effectue un zoom avant sur une étape de zoom ; CTRL+clic permet d’effectuer un zoom arrière sur une étape de zoom. Si vous <span class="codeph"> réinitialisez </span> , un seul clic sur l’image réinitialise le zoom au niveau de zoom initial. Dans le cas de <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est supérieur ou égal à la limite spécifiée, sinon un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-edcfcd6c0bd24ac093442c56450b3c97}

Facultatif.

## Par défaut {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] sur les ordinateurs de bureau; [!DNL `none`] sur les périphériques tactiles.

## Exemple {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]