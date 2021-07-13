---
description: Indique si la visionneuse commence à charger le contenu vidéo avant le démarrage de la lecture.
solution: Experience Manager
title: Video360Player.preload
feature: Dynamic Media Classic,Visionneuses,SDK/API,vidéo 360 VR
role: Developer,User
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 6%

---

# Video360Player.preload{#video-player-preload}

Indique si la visionneuse commence à charger le contenu vidéo avant le démarrage de la lecture.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Si elle est définie sur <span class="codeph"> 1 </span>, la vidéo commence à être téléchargée juste après la définition de la ressource. sinon, le préchargement ne démarre qu’une fois la lecture lancée par l’utilisateur final ou un appel API. </p> <p>Si elle est définie sur <span class="codeph"> 0 </span>, certaines fonctionnalités peuvent ne pas fonctionner avant le début de la lecture. en particulier, l’opération de recherche ne met pas à jour la image vidéo. Si l’image d’affiche est désactivée, la visionneuse s’affiche comme une zone vide au lieu de la première image vidéo. </p> <p>Notez que la désactivation du préchargement vidéo peut être ignorée dans certaines versions des navigateurs Internet Explorer 11 et Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
