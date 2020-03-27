---
description: 'null'
seo-description: 'null'
seo-title: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
topic: Dynamic media
uuid: b5dfb326-fbd8-4220-a44c-0d4f80b2a8fa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Chaîne de commande de diffusion d’images appliquée à toutes les nuances. Si elle est spécifiée dans l'URL, veillez à coder HTTP toutes les occurrences de <span class="codeph"> &amp;</span> et <span class="codeph"> =</span> en tant que <span class="codeph"> %26</span> et <span class="codeph"> %3D, respectivement.</span> </p> <p> <p>Remarque :  Les commandes de manipulation de dimensionnement d’image ne sont pas prises en charge. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Aucune

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

Lorsqu’elle est spécifiée dans l’URL de la visionneuse.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsqu’elle est spécifiée dans les données de configuration.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
