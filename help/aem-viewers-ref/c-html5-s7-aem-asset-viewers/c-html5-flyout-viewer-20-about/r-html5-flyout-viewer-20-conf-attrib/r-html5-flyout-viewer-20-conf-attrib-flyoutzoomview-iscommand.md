---
title: FlyoutZoomView.iscommand
description: FlyoutZoomView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b23918b5-5fc6-4038-b6f5-519198a96f86
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 5%

---

# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> </p> <p>Chaîne de commande de la Diffusion d’images appliquée à l’image principale FlyoutZoomView et à la vue agrandie. Si elle est spécifiée dans l'URL, veillez à encoder en HTTP toutes les occurrences de <span class="codeph"> &amp;</span> et <span class="codeph"> =</span> en <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement. </p> <p> <p>Remarque : les commandes de manipulation de dimensionnement d’image ne sont pas prises en charge. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

Aucune

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

Lorsqu’elle est spécifiée dans l’URL de la visionneuse :

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Lorsqu’il est spécifié dans les données de configuration :

`iscommand=op_sharpen=1&op_colorize=0xff0000`
