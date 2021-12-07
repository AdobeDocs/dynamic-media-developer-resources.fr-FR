---
title: videoServerUrl
description: Commande URL pour la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---

# videoServerUrl{#videoserverurl}

Commande URL pour la visionneuse de vidéos avec recadrage intelligent.

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Chemin d’accès racine du serveur vidéo. Si aucun domaine n’est spécifié, le domaine à partir duquel la page est diffusée est appliqué à la place. La résolution standard du chemin d’accès URI s’applique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif. Inutile pour l’utilisation standard de SaaS.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
