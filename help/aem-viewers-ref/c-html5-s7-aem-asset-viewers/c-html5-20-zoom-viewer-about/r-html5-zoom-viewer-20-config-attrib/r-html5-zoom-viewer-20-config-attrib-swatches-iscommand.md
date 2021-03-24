---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
feature: Dynamic Media Classic, Visionneuses, SDK/API, Zoom
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 7%

---


# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Chaîne de commande Diffusion d’images appliquée à toutes les nuances. Si elle est spécifiée dans l’URL, veillez à coder par HTTP toutes les occurrences de <span class="codeph"> &amp;</span> et <span class="codeph"> =</span> en <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement. </p> <p> <p>Remarque :  Les commandes de manipulation de dimensionnement d’image ne sont pas prises en charge. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

Aucune

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

Lorsqu’elle est spécifiée dans l’URL de la visionneuse.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsqu’elle est spécifiée dans les données de configuration.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
