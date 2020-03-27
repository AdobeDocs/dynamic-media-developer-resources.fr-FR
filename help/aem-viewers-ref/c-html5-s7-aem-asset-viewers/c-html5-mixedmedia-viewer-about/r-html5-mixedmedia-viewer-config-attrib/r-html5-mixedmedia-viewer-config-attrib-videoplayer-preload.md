---
description: Indique si la visionneuse commence à charger le contenu vidéo avant le  de lecture.
seo-description: Indique si la visionneuse commence à charger le contenu vidéo avant le  de lecture.
seo-title: VideoPlayer.preload
solution: Experience Manager
title: VideoPlayer.preload
topic: Dynamic media
uuid: 7fd801cf-8307-4b4e-a338-aa4d62b86d2f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.preload{#videoplayer-preload}

Indique si la visionneuse commence à charger le contenu vidéo avant le  de lecture.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Si elle est définie sur <span class="codeph"> 1, </span> le téléchargement de la vidéo commence juste après la définition de la ressource ; dans le cas contraire, préchargez le uniquement une fois que la lecture a été initiée par l’utilisateur final ou un appel d’API. </p> <p>Si cette valeur est définie sur <span class="codeph"> 0, </span> certaines fonctionnalités ne fonctionneront pas avant la  de lecture ; plus précisément, l’opération de recherche ne met pas à jour la trame vidéo. Si l’image d’affiche est désactivée, la visionneuse affiche une zone vide au lieu de la première image vidéo. </p> <p>Gardez à l’esprit que la désactivation du préchargement vidéo peut être ignorée sur certaines versions des navigateurs Internet Explorer 11 et Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
