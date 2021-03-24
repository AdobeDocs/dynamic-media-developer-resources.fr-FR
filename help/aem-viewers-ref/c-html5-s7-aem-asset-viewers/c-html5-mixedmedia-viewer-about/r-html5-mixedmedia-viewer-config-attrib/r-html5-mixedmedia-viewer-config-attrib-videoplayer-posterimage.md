---
description: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
feature: Dynamic Media Classic, Visionneuses, SDK/API, Combiner des visionneuses de supports
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
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

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Aucune

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
