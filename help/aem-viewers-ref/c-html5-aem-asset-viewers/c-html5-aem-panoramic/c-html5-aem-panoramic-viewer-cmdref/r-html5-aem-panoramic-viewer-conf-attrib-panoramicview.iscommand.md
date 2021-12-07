---
title: PanoramicView.iscommand
description: Attribut de configuration de la visionneuse panoramique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

Attribut de configuration de la visionneuse panoramique.

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Chaîne de commande de diffusion d’images appliquée à l’image.  Si elle est spécifiée dans l’URL, veillez à encoder HTTP toutes les occurrences de <span class="codeph"> &amp;</span> et <span class="codeph"> =</span> as <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

Aucune valeur par défaut.

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Lorsqu’il est spécifié dans l’URL de la visionneuse.

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

Lorsque spécifié dans les données de configuration.

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
