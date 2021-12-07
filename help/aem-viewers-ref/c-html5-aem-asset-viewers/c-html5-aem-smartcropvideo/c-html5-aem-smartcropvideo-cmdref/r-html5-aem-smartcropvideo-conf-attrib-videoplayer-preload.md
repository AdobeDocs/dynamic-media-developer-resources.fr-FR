---
title: SmartCropVideoPlayer.preload
description: Indique si la visionneuse commence à charger le contenu vidéo avant le démarrage de la lecture.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

Indique si la visionneuse commence à charger le contenu vidéo avant le démarrage de la lecture.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Si la variable est définie sur <span class="codeph"> 1 </span> la vidéo commence à être téléchargée juste après la définition de la ressource ; sinon, le préchargement ne démarre qu’une fois la lecture lancée par l’utilisateur final ou un appel API. </p> <p>Si la variable est définie sur <span class="codeph"> 0 </span> certaines fonctions peuvent ne pas fonctionner tant que la lecture ne recommence pas ; en particulier, l’opération de recherche ne met pas à jour la image vidéo. Si l’image d’affiche est désactivée, la visionneuse s’affiche comme une zone vide au lieu de la première image vidéo. </p> <p>La désactivation du préchargement vidéo peut être ignorée dans certaines versions des navigateurs Internet Explorer 11 et Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
