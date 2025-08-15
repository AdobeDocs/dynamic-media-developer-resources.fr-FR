---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3336c4d2-0d1d-4c6f-8163-8a84a8be8c20
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Aucune

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

Lorsque cela est spécifié dans l’URL de la visionneuse.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsque cela est indiqué dans les données de configuration.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
