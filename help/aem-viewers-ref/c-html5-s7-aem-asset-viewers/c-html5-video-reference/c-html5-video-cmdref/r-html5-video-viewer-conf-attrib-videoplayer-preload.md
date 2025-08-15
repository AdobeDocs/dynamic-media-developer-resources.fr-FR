---
title: VideoPlayer.preload
description: Indique si la visionneuse commence à charger le contenu vidéo avant le début de la lecture.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: cee887f6-bbd9-46dd-aa41-03493596fcf4
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# VideoPlayer.preload{#videoplayer-preload}

Indique si la visionneuse commence à charger le contenu vidéo avant le début de la lecture.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Si la valeur est définie sur <span class="codeph"> 1, </span> la vidéo commence à être téléchargée juste après la définition de la ressource. Dans le cas contraire, le préchargement ne commence qu’une fois la lecture lancée par l’utilisateur final ou un appel API. </p> <p>Si elle est définie sur <span class="codeph"> 0 </span> certaines fonctionnalités peuvent ne pas fonctionner jusqu’au début de la lecture ; en particulier, l’opération de recherche ne met pas à jour l’image vidéo. Si l’image d’affiche est désactivée, la visionneuse s’affiche comme une zone vide au lieu de la première image vidéo. </p> <p>La désactivation du préchargement vidéo peut être ignorée sur certaines versions des navigateurs Internet Explorer 11 et Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
