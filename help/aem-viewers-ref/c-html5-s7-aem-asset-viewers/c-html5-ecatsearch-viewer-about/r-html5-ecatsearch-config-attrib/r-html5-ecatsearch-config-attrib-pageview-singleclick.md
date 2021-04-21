---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de zoom d’un simple clic/clic. La définition de <span class="codeph"> none </span> désactive le zoom par clic/clic. Si la valeur <span class="codeph"> zoom </span> est définie, le fait de cliquer sur l’image effectue un zoom avant sur une étape de zoom ; CTRL+clic permet d’effectuer un zoom arrière sur une étape de zoom. Si vous définissez <span class="codeph"> reset </span>, un seul clic sur l’image réinitialise le zoom au niveau de zoom initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est égal ou supérieur à la limite spécifiée, sinon un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-edcfcd6c0bd24ac093442c56450b3c97}

Facultatif.

## Par défaut {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] sur les ordinateurs de bureau ;  [!DNL `none`] sur les périphériques tactiles.

## Exemple {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]