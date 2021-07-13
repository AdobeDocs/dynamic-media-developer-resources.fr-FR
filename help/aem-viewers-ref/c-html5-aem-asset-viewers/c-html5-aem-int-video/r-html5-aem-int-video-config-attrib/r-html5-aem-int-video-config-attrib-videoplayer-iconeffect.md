---
description: Attribut de configuration de la visionneuse de vidéos interactives.
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéos interactives
role: Developer,User
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 4%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Attribut de configuration de la visionneuse de vidéos interactives.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Permet à IconEffect d’être affiché en haut de la vidéo lorsque la vidéo est en pause. Sur certains périphériques, des contrôles natifs sont utilisés. Dans ce cas, le modificateur <span class="codeph"> iconEffet</span> est ignoré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le nombre maximal de fois où IconEffect apparaît et réapparaît. Une valeur <span class="codeph"> -1</span> indique que l’icône réapparaît indéfiniment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p> Spécifie la durée d’affichage ou de masquage de l’animation, en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Définit le nombre de secondes pendant lesquelles IconEffect reste entièrement visible avant son masquage automatique. C’est-à-dire le temps qui suit la fin du fondu dans l’animation et avant le début de l’animation de fondu. Définissez cette variable sur <span class="codeph"> 0</span> pour désactiver le comportement de masquage automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
