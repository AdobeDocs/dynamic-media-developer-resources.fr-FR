---
description: Attribut de configuration de la visionneuse Video360.
solution: Experience Manager
title: VideoScrubber.timepattern
feature: Dynamic Media Classic,Visionneuses,SDK/API,vidéo 360 VR
role: Developer,User
exl-id: f438a06b-6cf4-4bcd-9c4a-ed56f6a9c639
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

Attribut de configuration de la visionneuse Video360.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Définit le modèle de la durée affichée dans la bulle temporelle, où <span class="codeph"> h</span> correspond aux heures, <span class="codeph"> m</span> aux minutes et <span class="codeph"> s</span> aux secondes. </p> <p>Le nombre de lettres utilisé pour chaque unité de temps détermine le nombre de chiffres à afficher pour l’unité. Si le nombre ne peut pas tenir dans les chiffres donnés, la valeur équivalente est affichée dans l’unité suivante. </p> <p>Par exemple, si l’heure actuelle du film est de 67 minutes et 5 secondes, le modèle d’heure <span class="codeph"> m:ss</span> s’affiche sous la forme 67:05. La même heure est affichée sous la forme 1:07:5 si le modèle de temps donné est <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```
