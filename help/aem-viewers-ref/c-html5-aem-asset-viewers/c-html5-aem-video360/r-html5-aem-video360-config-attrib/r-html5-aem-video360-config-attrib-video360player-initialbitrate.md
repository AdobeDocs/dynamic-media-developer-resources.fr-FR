---
description: Attribut de configuration pour la visionneuse Video360.
seo-description: Attribut de configuration pour la visionneuse Video360.
seo-title: Video360Player.initialbitrate
solution: Experience Manager
title: Video360Player.initialbitrate
uuid: a23fa941-6dd2-41c0-aca9-06f0cdb027b1
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---


# Video360Player.initialbitrate{#video-player-initialbitrate}

Attribut de configuration pour la visionneuse Video360.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Définit le débit vidéo (en kbits par seconde ou en kbits/s) utilisé pour la lecture initiale de la vidéo sur un ordinateur de bureau. </p> <p>Si cette valeur de débit n’existe pas dans la visionneuse de vidéos adaptative, le lecteur vidéo se début avec la vidéo dont le débit est le plus faible suivant. </p> <p>Si elle est définie sur <span class="codeph"> 0</span>, le lecteur vidéo début à partir du débit le plus faible possible. </p> <p>Applicable uniquement aux systèmes qui ne prennent pas en charge les vidéos HTML5 HLS en mode natif (comme Firefox, Chrome et Internet Explorer 11 sous Windows 10) et lorsque le mode de lecture est défini sur auto. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```

