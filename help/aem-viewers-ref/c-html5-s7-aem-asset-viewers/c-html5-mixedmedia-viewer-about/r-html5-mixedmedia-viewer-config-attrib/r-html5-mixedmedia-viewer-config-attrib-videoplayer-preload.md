---
description: Indique si la visionneuse commence à charger du contenu vidéo avant les débuts de lecture.
solution: Experience Manager
title: VideoPlayer.preload
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---


# VideoPlayer.preload{#videoplayer-preload}

Indique si la visionneuse commence à charger du contenu vidéo avant les débuts de lecture.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Si elle est définie sur <span class="codeph"> 1 </span>, la vidéo commence à être téléchargée juste après la définition de la ressource ; sinon, préchargez les débuts uniquement après le début de la lecture par l’utilisateur final ou un appel d’API. </p> <p>Si elle est définie sur <span class="codeph"> 0 </span>, certaines fonctions ne peuvent pas fonctionner avant les débuts de lecture ; plus précisément, l'opération de recherche ne mettra pas à jour la trame vidéo. Si l’image d’affiche est désactivée, la visionneuse s’affiche comme une zone vide au lieu de la première image vidéo. </p> <p>Notez que la désactivation du préchargement vidéo peut être ignorée dans certaines versions des navigateurs Internet Explorer 11 et Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
