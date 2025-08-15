---
title: VideoPlayer.iconeffect
description: VideoPlayer.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 8371cb69-4cd9-457b-bd8c-e4167fc67600
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`comptage`*][, *`fondu`*][, *`enchaîné Masquer automatiquement`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Permet à l’effet IconEffect de s’afficher au-dessus de la vidéo lorsque celle-ci est en pause. Sur certains appareils, des contrôles natifs sont utilisés. Dans ce cas, le modificateur iconeffect <span class="codeph"></span> est ignoré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> compter</span> </span> </p> </td> 
   <td colname="col2"> <p> Spécifie le nombre maximal de fois où l’effet IconEffect apparaît et réapparaît. La valeur <span class="codeph"> -1</span> indique que l’icône réapparaît indéfiniment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> se faner</span> </span> </p> </td> 
   <td colname="col2"> <p> Définit la durée d’affichage ou de masquage de l’animation, en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Masquer</span> automatiquement </span> </p> </td> 
   <td colname="col2"> <p> Définit le nombre de secondes pendant lesquelles l’effet IconEffect reste visible avant de se masquer automatiquement. C’est-à-dire le temps après la fin de l’animation en fondu et avant le début de l’animation en fondu. Un paramètre de <span class="codeph"> 0</span> désactive le comportement de masquage automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
