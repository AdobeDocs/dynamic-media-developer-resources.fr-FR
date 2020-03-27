---
description: Attribut de configuration pour la visionneuse vidéo.
seo-description: Attribut de configuration pour la visionneuse vidéo.
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 1ba6f24a-77bb-41ef-a831-a7ac817abd73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Attribut de configuration pour la visionneuse vidéo.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Permet à IconEffect de s’afficher au-dessus de la vidéo lorsque la vidéo est en pause. Sur certains périphériques, des commandes natives sont utilisées. Dans ce cas, le modificateur <span class="codeph"> iconeffect</span> est ignoré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le nombre maximal de fois que l’effet IconEffect apparaît et réapparaît. La valeur <span class="codeph"> -1</span> indique que l’icône réapparaît indéfiniment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p> Spécifie la durée d’affichage ou de masquage de l’animation, en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoMasquer</span></span> </p> </td> 
   <td colname="col2"> <p> Définit le nombre de secondes pendant lesquelles IconEffect reste visible avant le masquage automatique. C’est-à-dire le moment où l’animation en fondu est terminée et avant le  d’animation en fondu. Un paramètre de <span class="codeph"> 0</span> désactive le comportement de masquage automatique. </p> </td> 
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

