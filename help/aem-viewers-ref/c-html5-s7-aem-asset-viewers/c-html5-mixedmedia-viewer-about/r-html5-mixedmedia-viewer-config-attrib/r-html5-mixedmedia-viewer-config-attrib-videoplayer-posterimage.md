---
title: VideoPlayer.posterimage
description: VideoPlayer.posterimage
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aucun|[<span class="varname"> image_id</span>][ ?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> L’image à afficher sur la première image avant que la vidéo ne commence à être lue, résolue par rapport à <span class="codeph">’URL du serveur</span>. Si spécifié dans l’URL, codez en HTTP les éléments suivants : </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> comme <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> comme <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> comme <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Si la valeur <span class="codeph"><span class="varname"> image_id</span></span> est omise, le composant tente d’utiliser l’image d’affiche par défaut pour cette ressource à la place. </p> <p>Lorsque la vidéo est spécifiée comme chemin d’accès, l’ID de catalogue d’images d’affiche par défaut est dérivé du chemin d’accès de la vidéo en tant que paire <span class="codeph"> catalog_id/image_id</span> où <span class="codeph"> catalog_id</span> correspond au premier jeton du chemin d’accès. Et, <span class="codeph"> image_id</span> est le nom de la vidéo dont l’extension est supprimée. Si l’image avec cet identifiant n’existe pas, l’image d’affiche n’est pas affichée. </p> <p>Pour empêcher l’affichage de l’image d’affiche par défaut, spécifiez <span class="codeph"> aucune</span> comme valeur de l’image d’affiche. Si seules les <span class="codeph"><span class="varname"> isCommands</span></span> sont spécifiées, les commandes sont appliquées à l’image d’affiche par défaut avant l’affichage de l’image. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Aucune

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
