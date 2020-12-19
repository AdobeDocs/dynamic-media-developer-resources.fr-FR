---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: a403d44d-d5b5-4d09-876e-39146585704f
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 4%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Attribut de configuration pour la visionneuse de vidéos interactive.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Permet à IconEffect d’être affiché au-dessus de la vidéo lorsque celle-ci est en pause. Sur certains périphériques, des commandes natives sont utilisées. Dans ce cas, le modificateur <span class="codeph"> iconeffect</span> est ignoré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le nombre maximal de fois où IconEffect apparaît et réapparaît. La valeur <span class="codeph"> -1</span> indique que l’icône réapparaît indéfiniment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fondre</span></span> </p> </td> 
   <td colname="col2"> <p> Indique la durée d’affichage ou de masquage de l’animation, en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Définit le nombre de secondes pendant lesquelles IconEffect reste entièrement visible avant de se masquer automatiquement. En d’autres termes, le temps après le fondu dans l’animation est terminé et avant le fondu des débuts d’animation. Définissez cette variable sur <span class="codeph"> 0</span> pour désactiver le comportement de masquage automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
