---
title: SpinView.iscommand
description: SpinView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 6924e133-31f4-4c00-8bcc-25749b52a68d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> Chaîne de commande de diffusion d’images appliquée à l’image à 360°. Si spécifié dans l’URL, toutes les occurrences de <span class="codeph"> &amp;</span> et <span class="codeph"> =</span> doit être codé en HTTP en tant que <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement. </p> <p> <p>Remarque : Les commandes de manipulation de dimensionnement d’image ne sont pas prises en charge. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

Aucune

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

Lorsqu’il est spécifié dans l’URL de la visionneuse :

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsque spécifié dans les données de configuration :

`iscommand=op_sharpen=1&op_colorize=0xff0000`
