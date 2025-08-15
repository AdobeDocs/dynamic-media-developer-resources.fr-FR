---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: b5b0acab-4e11-4f6a-8cb1-be6d683d7384
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`Commande isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Commande isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Chaîne de commande Diffusion d’images appliquée à toutes les nuances. S’il est spécifié dans l’URL, veillez à coder HTTP toutes les occurrences de <span class="codeph"> &amp;</span> et = <span class="codeph"></span> comme <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement. </p> <p> <p>Remarque : les commandes de manipulation de dimensionnement d’image ne sont pas prises en charge. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

Aucune

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

Lorsque cela est spécifié dans l’URL de la visionneuse.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsque cela est indiqué dans les données de configuration.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
