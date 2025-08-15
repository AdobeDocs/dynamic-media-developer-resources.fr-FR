---
title: ZoomView.iscommand
description: ZoomView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: d1f54ef2-4ed4-4fb6-9913-98bf194f9afc
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`Commande isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Commande isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Chaîne de commande de diffusion d’images appliquée au zoom de l’image. Si elles sont spécifiées dans l’URL, toutes les occurrences de &amp; et = doivent être codées en HTTP en tant que <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement.<span class="codeph"> </span><span class="codeph"> </span> </p> <p> <p>Remarque : les commandes de manipulation de dimensionnement d’image ne sont pas prises en charge. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-50bcd15223174bb79ce08b31ea03d682}

Facultatif.

## Par défaut {#section-7564169749ff4a4996049ea1148cb2a5}

Aucune

## Exemple {#section-96e69b70365f461dae4399e49044ea2f}

Lorsque cela est spécifié dans l’URL de la visionneuse :

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsque cela est spécifié dans les données de configuration :

`iscommand=op_sharpen=1&op_colorize=0xff0000`
