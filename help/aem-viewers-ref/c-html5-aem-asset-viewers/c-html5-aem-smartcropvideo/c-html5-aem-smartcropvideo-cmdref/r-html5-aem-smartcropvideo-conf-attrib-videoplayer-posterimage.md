---
title: SmartCropVideoPlayer.posterimage
description: Attribut de configuration pour la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ff4f8e2c-b9c3-4fba-b3f0-fa1eaddcd8c0
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

Attribut de configuration pour la visionneuse de vidéos avec recadrage intelligent.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *` `*][? *`image_id isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Aucun|<span class="varname"> [ image_id</span>][ ?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Image à afficher sur la première image avant le début de la lecture de la vidéo, résolue par rapport <span class="codeph"> à serverurl</span>. Si l’URL l’indique, encodez HTTP-encode ce qui suit : </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> en tant que <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> et</span> sous % <span class="codeph"> 26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"></span>= en tant que <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Si la valeur image_id <span class="codeph"><span class="varname"></span></span> est omise, le composant tente d’utiliser l’image d’affiche par défaut pour cette ressource. </p> <p>Lorsque la vidéo est spécifiée en tant que chemin, l’ID de catalogue d’images d’affiche par défaut est dérivé du chemin de la vidéo en tant que <span class="codeph"> paire catalog_id/image_id</span> . Le <span class="codeph"> catalog_id</span> correspond au premier jeton du chemin et <span class="codeph"> image_id</span> est le nom de la vidéo avec l’extension supprimée. Si l’image avec cet ID n’existe pas, l’image de l’affiche n’est pas affichée. </p> <p>Pour empêcher l’affichage de l’image d’affiche par défaut, spécifiez <span class="codeph"> aucune</span> comme valeur d’image d’affiche. Si seules les <span class="codeph"><span class="varname"> isCommands sont spécifiées</span></span> , les commandes sont appliquées à l’image d’affiche par défaut avant l’affichage de l’image. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

Aucune

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
