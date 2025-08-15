---
title: EmbedShare.embedsizes
description: Attribut de configuration pour la visionneuse Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 3a6c23dd-5e2c-4149-aa24-37d445128125
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 5%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Attribut de configuration pour la visionneuse Video360.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`width`*, *`height`*[,0|1][; *`width`*, *`height`*[,0|1]]`

Spécifie une liste de tailles incorporées pour la zone de liste déroulante de taille dans la boîte de dialogue modale de partage incorporé.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur <span class="varname"> </span> </span> </p> </td> 
   <td colname="col2"> <p> Largeur d’incorporation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hauteur </span> </span> </p> </td> 
   <td colname="col2"> <p>Hauteur d’incorporation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Indique si cet élément de liste doit être initialement présélectionné dans la zone de liste. </p> </td> 
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
