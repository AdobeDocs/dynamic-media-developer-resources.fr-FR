---
description: Attribut de configuration pour la visionneuse Video360.
seo-description: Attribut de configuration pour la visionneuse Video360.
seo-title: EmbedShare.embedsizes
solution: Experience Manager
title: EmbedShare.embedsizes
topic: Dynamic media
uuid: d3eea508-fb1e-4147-b853-a16f51725dd7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 11%

---


# EmbedShare.embedsizes{#embedshare-embedsizes}

Attribut de configuration pour la visionneuse Video360.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *``*, *``*[,0|1][; *``*, *`largeurhauteurLargeurLargeur`*[,0|1]]`

Spécifie une liste de tailles incorporées pour la zone combinée de taille dans la boîte de dialogue modale de partage incorporée.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> Largeur intégrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>Incorporer la hauteur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Indique si cet élément de liste doit être initialement présélectionné dans la zone combinée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```

