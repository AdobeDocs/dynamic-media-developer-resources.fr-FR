---
title: VideoPlayer.iconeffect
description: Attribut de configuration de la visionneuse de vidéos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b283b495-ee28-4f9d-ad4d-b14ac2f9a1a2
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Attribut de configuration de la visionneuse de vidéos.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Active l’IconEffect pour qu’il s’affiche au-dessus de la vidéo lorsque celle-ci est en pause. Sur certains appareils, des contrôles natifs sont utilisés. Dans ce cas, le modificateur <span class="codeph"> iconeffect</span> est ignoré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> nombre </span> </span> </p> </td> 
   <td colname="col2"> <p> Indique le nombre maximal de fois où IconEffect apparaît et réapparaît. Une valeur <span class="codeph"> -1</span> indique que l’icône réapparaît indéfiniment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fondu</span> </span> </p> </td> 
   <td colname="col2"> <p> Spécifie la durée d'affichage ou de masquage de l'animation, en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Définit le nombre de secondes pendant lesquelles IconEffect reste visible avant d’effectuer le masquage automatique. En d'autres termes, le temps écoulé entre la fin de l'animation de fondu avant le début de l'animation de fondu arrière. Un paramètre de <span class="codeph"> 0</span> désactive le comportement de masquage automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
