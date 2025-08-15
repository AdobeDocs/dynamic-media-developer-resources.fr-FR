---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffe77be7-bf12-4e9d-9355-2857d366d14e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aucun|zoom|réinitialisation|réinitialisationZoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions d’un simple clic/appuyer sur le zoom. La définition sur <span class="codeph"> aucun </span> désactive le zoom d’un clic/appuyer unique. Si vous souhaitez <span class="codeph"> zoomer </span> , cliquer sur l’image effectue un zoom d’un pas de zoom. CTRL+clic effectue un zoom arrière d’un pas de zoom. Le paramètre de <span class="codeph"> réinitialisation </span> provoque un simple clic sur l’image pour réinitialiser le zoom au niveau de zoom initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est égal ou supérieur à la limite spécifiée, sinon le zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-edcfcd6c0bd24ac093442c56450b3c97}

Facultatif.

## Par défaut {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] sur les ordinateurs de bureau ; [!DNL `none`] sur les appareils tactiles.

## Exemple {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]
