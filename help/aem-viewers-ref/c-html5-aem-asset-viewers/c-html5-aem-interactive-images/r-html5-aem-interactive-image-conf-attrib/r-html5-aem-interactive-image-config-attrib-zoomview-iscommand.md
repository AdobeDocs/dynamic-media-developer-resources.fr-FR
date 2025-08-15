---
title: ZoomView.iscommand
description: Chaîne de commande de diffusion d’images appliquée au zoom de l’image.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 1c24973e-1daf-4d9d-b97c-fb6a18f506ed
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# ZoomView.iscommand{#zoomview-iscommand}

Chaîne de commande de diffusion d’images appliquée au zoom de l’image.

` [ZoomView.|<containerId>_zoomView.]iscommand= *`Commande isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Commande isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Si elles sont spécifiées dans l’URL, toutes les occurrences de &amp; et = doivent être codées en HTTP en tant que <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement.<span class="codeph"> </span><span class="codeph"> </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

Aucune

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

Lorsque cela est spécifié dans l’URL de la visionneuse :

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsque cela est spécifié dans les données de configuration :

`iscommand=op_sharpen=1&op_colorize=0xff0000`
