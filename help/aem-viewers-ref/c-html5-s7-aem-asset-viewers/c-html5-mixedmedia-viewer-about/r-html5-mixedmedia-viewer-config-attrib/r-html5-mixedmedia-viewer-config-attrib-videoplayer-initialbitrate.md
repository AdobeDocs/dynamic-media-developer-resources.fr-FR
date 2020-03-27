---
description: 'null'
seo-description: 'null'
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: 11426516-8336-4186-84b4-15ce5ec7e764
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> valeur </span></span> </p> </td> 
   <td colname="col2"> <p>Définit le débit vidéo en kbits par seconde ou en kbit/s utilisé pour la lecture initiale de la vidéo sur les ordinateurs de bureau. </p> <p>Si cette valeur de débit n’existe pas dans la visionneuse de vidéos adaptative, le lecteur vidéo  la vidéo dont le débit est le plus faible suivant. </p> <p>Si cette valeur est définie sur <span class="codeph"> </span> 0, le du lecteur vidéo  du débit le plus faible possible. Applicable uniquement pour les systèmes qui ne prennent pas en charge les vidéos HTML5 HLS en mode natif (c’est-à-dire les navigateurs Firefox, Chrome et Internet Explorer 11 sous Windows 10) et lorsque le mode de lecture est défini sur <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
