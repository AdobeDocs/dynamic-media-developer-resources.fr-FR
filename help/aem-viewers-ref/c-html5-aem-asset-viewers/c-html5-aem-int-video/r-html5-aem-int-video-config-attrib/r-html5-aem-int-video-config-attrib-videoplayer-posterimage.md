---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
solution: Experience Manager
title: VideoPlayer.posterimage
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéos interactives
role: Développeur, Professionnel
exl-id: 17c1220d-f2a4-4729-84e2-b9f6f5732423
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

Attribut de configuration pour la visionneuse de vidéos interactive.

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Image à afficher sur la première image avant la lecture des débuts de la vidéo, résolue par rapport à <span class="codeph"> serverurl</span>. Si elle est spécifiée dans l’URL, codez les éléments suivants par HTTP : </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> comme  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> comme  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Si la valeur <span class="codeph"><span class="varname"> image_id</span></span> est omise, le composant tente à la place d’utiliser l’image d’affiche par défaut pour cette ressource. </p> <p>Lorsque la vidéo est spécifiée en tant que chemin d’accès, l’ID de catalogue des images d’affiche par défaut est dérivé du chemin d’accès de la vidéo en tant que paire <span class="codeph"> catalog_id/image_id</span> où <span class="codeph"> catalog_id</span> correspond au premier jeton du chemin et <span class="codeph"> image_id</span> est le nom de la vidéo dont l’extension a été supprimée. Si l’image avec cet ID n’existe pas, l’image d’affiche n’est pas affichée. </p> <p>Pour empêcher l’affichage de l’image d’affiche par défaut, spécifiez <span class="codeph"> none</span> comme valeur d’image d’affiche. Si seuls les <span class="codeph"><span class="varname"> isCommands</span></span> sont spécifiés, les commandes sont appliquées à l’image d’affiche par défaut avant l’affichage de l’image. </p> </td> 
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
