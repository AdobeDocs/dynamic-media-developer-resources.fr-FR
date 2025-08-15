---
title: SmartCropVideoPlayer.preload
description: Indique si la visionneuse commence à charger le contenu vidéo avant le début de la lecture.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7a83a02e-7b75-4f15-b8c1-aa7b64e6d3bd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

Indique si la visionneuse commence à charger le contenu vidéo avant le début de la lecture.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Si la vidéo est définie sur <span class="codeph"> 1 </span> , le téléchargement de la vidéo commence juste après la définition de la ressource ; sinon, le préchargement ne démarre qu’après que la lecture a été lancée par l’utilisateur final ou un appel d’API. </p> <p>Si elle est définie sur <span class="codeph"> 0 </span> , certaines fonctionnalités peuvent ne pas fonctionner tant que la lecture ne recommence. Plus précisément, l’opération de recherche ne met pas à jour l’image vidéo. Si l’image de l’affiche est désactivée, la visionneuse s’affiche sous la forme d’une zone vide au lieu de la première image vidéo. </p> <p>La désactivation du préchargement vidéo peut être ignorée sur certaines versions des navigateurs Internet Explorer 11 et Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
