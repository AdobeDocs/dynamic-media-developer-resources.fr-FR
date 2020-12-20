---
description: Attribut de configuration pour la visionneuse de vidéos.
seo-description: Attribut de configuration pour la visionneuse de vidéos.
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: 44c86fdb-7e96-4d90-99a1-3b0670d3696f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

Attribut de configuration pour la visionneuse de vidéos.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Définit le modèle de la durée affichée dans la bulle de temps, où <span class="codeph"> h</span> est heures, <span class="codeph"> m</span> est minutes et <span class="codeph"> s</span> est secondes. </p> <p>Le nombre de lettres utilisées pour chaque unité de temps détermine le nombre de chiffres à afficher pour l'unité. Si le nombre ne peut pas tenir dans les chiffres donnés, la valeur équivalente est affichée dans l’unité suivante. </p> <p>Par exemple, si l’heure actuelle du film est de 67 minutes et 5 secondes, le modèle de temps <span class="codeph"> m:ss</span> s’affiche sous la forme 67:05. La même heure s’affiche sous la forme 1:07:5 si le modèle d’heure donné est <span class="codeph"> h:mm:s</span>. </p> </td> 
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

