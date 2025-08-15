---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d92e56ae-2bb6-46f6-b0f7-64b867492a37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# PageView.zoomstep{#pageview-zoomstep}

[!DNL `[PageView.|<containerId>_pageView.]zoomstep= *`Limite d’étape`*[, *``*]`]

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> pas</span></span> </p> </td> 
   <td colname="col2"> <p> Configure le nombre d’actions de zoom avant et de zoom arrière nécessaires pour multiplier par deux la résolution ou la diminuer. Le changement de résolution pour chaque action de zoom est de 2^1 par étape. Définissez ce paramètre sur <span class="codeph"> 0</span> pour effectuer un zoom en pleine résolution d’une simple action de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limite</span></span> </p> </td> 
   <td colname="col2"> <p> Spécifie la résolution de zoom maximale par rapport à l’image à pleine résolution. La valeur par défaut est <span class="codeph"> 1.0</span>, ce qui ne permet pas de zoomer au-delà de la pleine résolution. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-636d35a4791447039f1902973f568320}

Facultatif.

## Par défaut {#section-ad8a5fe2383e4c228bf177a41b53d921}

[!DNL `1,1`]

## Exemple {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]
