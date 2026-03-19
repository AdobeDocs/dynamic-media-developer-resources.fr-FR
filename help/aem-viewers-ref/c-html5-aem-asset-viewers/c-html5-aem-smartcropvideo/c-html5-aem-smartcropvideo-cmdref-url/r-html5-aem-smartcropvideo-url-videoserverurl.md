---
title: videoServerUrl
description: Commande d’URL de la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 9bd37d2c-c7ec-4f58-8328-45c0a156f330
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 5%

---

# videoServerUrl{#videoserverurl}

Commande d’URL de la visionneuse de vidéos avec recadrage intelligent.

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Chemin d’accès racine du serveur vidéo. Si aucun domaine n’est spécifié, le domaine à partir duquel la page est diffusée est appliqué à la place. La résolution de chemin d’URI standard s’applique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif. Non nécessaire pour une utilisation SaaS standard.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
