---
description: Chaîne de commande de diffusion d’images appliquée à l’image de zoom.
solution: Experience Manager
title: ZoomView.iscommand
feature: Dynamic Media Classic, Visionneuses, SDK/API, Images interactives
role: Développeur, Professionnel
exl-id: 1c24973e-1daf-4d9d-b97c-fb6a18f506ed
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 7%

---

# ZoomView.iscommand{#zoomview-iscommand}

Chaîne de commande de diffusion d’images appliquée à l’image de zoom.

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> Si elle est spécifiée dans l’URL, toutes les occurrences de <span class="codeph"> &amp;</span> et <span class="codeph"> =</span> doivent être codées en HTTP sous la forme <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

Aucune

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

Lorsqu’elle est spécifiée dans l’URL de la visionneuse :

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsque spécifié dans les données de configuration :

`iscommand=op_sharpen=1&op_colorize=0xff0000`
