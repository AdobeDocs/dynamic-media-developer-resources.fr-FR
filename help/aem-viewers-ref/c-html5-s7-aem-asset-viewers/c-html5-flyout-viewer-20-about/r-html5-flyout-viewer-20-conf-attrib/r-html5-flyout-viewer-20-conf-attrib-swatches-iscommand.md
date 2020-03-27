---
description: 'null'
seo-description: 'null'
seo-title: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
topic: Dynamic media
uuid: a9928350-d9a9-49b0-8990-1f8b67d82f10
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

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

Aucune

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

Lorsqu’elle est spécifiée dans l’URL du lecteur de contenu :

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsqu’elle est spécifiée dans les données de configuration :

`iscommand=op_sharpen=1&op_colorize=0xff0000`
