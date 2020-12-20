---
description: Attribut de configuration pour la visionneuse Video360.
seo-description: Attribut de configuration pour la visionneuse Video360.
seo-title: Video360Player.posterimage
solution: Experience Manager
title: Video360Player.posterimage
topic: Dynamic media
uuid: a1adc3b7-2ea3-4f26-84f2-b5c2f4418038
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 14%

---


# Video360Player.posterimage{#video-player-posterimage}

Attribut de configuration pour la visionneuse Video360.

` [Video360Player.|<containerId>_video360Player.]posterimage=none|[? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Modificateurs de diffusion d’images qui contrôlent l’aspect de l’affiche. Si elle est spécifiée dans l’URL, codez les éléments suivants par HTTP : </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> comme  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> comme  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p> Ce modificateur fonctionne pour le contenu vidéo hébergé sur Dynamic Media Classic ou AEM Dynamic Media. </p> <p>Pour empêcher l’affichage de l’image d’affiche par défaut, spécifiez <span class="codeph"> none</span> comme valeur d’image d’affiche. </p> </td> 
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

