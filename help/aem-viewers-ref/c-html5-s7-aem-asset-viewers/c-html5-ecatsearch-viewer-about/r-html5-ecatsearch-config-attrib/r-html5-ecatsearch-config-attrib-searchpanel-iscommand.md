---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4e843866-75a5-4543-a275-e134b3aee75a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 8%

---

# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`Commande isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Commande isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Chaîne de commande du service d’images appliquée à toutes les miniatures. Si elles sont spécifiées dans l’URL, toutes les occurrences de &amp; et = doivent être codées en HTTP en tant que <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement.<span class="codeph"> </span><span class="codeph"> </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-df5a0604766b4ac2b9a6742b377e427c}

Facultatif.

## Par défaut {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Aucune

## Exemple {#section-813de2905d6c44c0991cfe0931581462}

Lorsque cela est spécifié dans l’URL de la visionneuse.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

Lorsque cela est spécifié dans les données de configuration.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
