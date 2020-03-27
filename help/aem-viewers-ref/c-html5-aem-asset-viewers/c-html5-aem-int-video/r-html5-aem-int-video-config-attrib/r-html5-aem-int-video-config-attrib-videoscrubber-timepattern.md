---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: dc2e7b18-abd7-4b53-a0c4-268ec9cf3cb4
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

Attribut de configuration pour la visionneuse de vidéos interactive.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Définit le modèle de temps affiché dans la bulle de temps, où <span class="codeph"> h</span> représente les heures, <span class="codeph"> m</span> les minutes et <span class="codeph"></span> sles secondes. </p> <p>Le nombre de lettres utilisé pour chaque unité de temps détermine le nombre de chiffres à afficher pour l’unité. Si le nombre ne peut pas tenir dans les chiffres donnés, la valeur équivalente est affichée dans l’unité suivante. </p> <p>Par exemple, si l’heure actuelle du film est de 67 minutes et 5 secondes, un modèle d’heure <span class="codeph"> m:ss</span> s’affiche sous la forme 67:05. La même heure est affichée comme 1:07:5 si le modèle de temps est <span class="codeph"> :mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```

