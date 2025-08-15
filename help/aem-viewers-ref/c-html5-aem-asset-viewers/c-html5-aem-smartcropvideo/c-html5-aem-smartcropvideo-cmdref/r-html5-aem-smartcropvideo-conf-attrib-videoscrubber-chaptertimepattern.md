---
title: VideoScrubber.chaptertimepattern
description: Attribut de configuration pour la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5552ed9e-d8fe-4723-a360-405b91e27f8e
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 2%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Attribut de configuration pour la visionneuse de vidéos avec recadrage intelligent.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h :]m|mm :s|ss</span> </p> </td> 
   <td colname="col2"> <p> Définit le modèle pour l’heure affichée dans la barre de titre du libellé du chapitre vidéo. <span class="codeph"> h </span> est heures, <span class="codeph"> m est minutes, </span> et<span class="codeph"> s</span> est secondes. </p> <p>Le nombre de lettres utilisées pour chaque unité de temps détermine le nombre de chiffres à afficher pour l’unité. Si le nombre ne peut pas entrer dans les chiffres donnés, la valeur équivalente est affichée dans l’unité suivante. </p> <p>Par exemple, si la durée actuelle du film est de 67 minutes et 5 secondes, le modèle <span class="codeph"> de temps m :ss</span> affiche 67:05. La même heure est affichée comme 1:07:5 si le modèle temporel donné est <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```
