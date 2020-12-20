---
description: 'null'
seo-description: 'null'
seo-title: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
topic: Dynamic media
uuid: 7496fea1-8a69-4749-ab4b-ae6d375441b8
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 13%

---


# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Chaîne de commande de diffusion d’images appliquée à toutes les miniatures. Si elle est spécifiée dans l’URL, toutes les occurrences de <span class="codeph"> &amp;</span> et <span class="codeph"> =</span> doivent être codées en HTTP sous la forme <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-df5a0604766b4ac2b9a6742b377e427c}

Facultatif.

## Par défaut {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Aucune

## Exemple {#section-813de2905d6c44c0991cfe0931581462}

Lorsqu’elle est spécifiée dans l’URL de la visionneuse.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

Lorsqu’elle est spécifiée dans les données de configuration.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
