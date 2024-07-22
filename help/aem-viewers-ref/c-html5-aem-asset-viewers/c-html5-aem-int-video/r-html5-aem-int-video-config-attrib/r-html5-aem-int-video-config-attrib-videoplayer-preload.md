---
title: VideoPlayer.preload
description: Indique si la visionneuse commence à charger le contenu vidéo avant le démarrage de la lecture.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: afabbfde-e003-4fee-a4ef-0fc4c43fd960
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# VideoPlayer.preload{#videoplayer-preload}

Indique si la visionneuse commence à charger le contenu vidéo avant le démarrage de la lecture.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Si celle-ci est définie sur <span class="codeph"> 1 </span>, le téléchargement de la vidéo commence juste après la définition de la ressource ; dans le cas contraire, le préchargement ne démarre qu’après le lancement de la lecture par l’utilisateur final ou un appel API. </p> <p>Si elle est définie sur <span class="codeph"> 0 </span>, certaines fonctionnalités peuvent ne pas fonctionner tant que la lecture n’a pas commencé. En particulier, l’opération de recherche ne met pas à jour la image vidéo. Si l’image d’affiche est désactivée, la visionneuse s’affiche comme une zone vide au lieu de la première image vidéo. </p> <p>La désactivation du préchargement vidéo peut être ignorée dans certaines versions des navigateurs Internet Explorer 11 et Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
