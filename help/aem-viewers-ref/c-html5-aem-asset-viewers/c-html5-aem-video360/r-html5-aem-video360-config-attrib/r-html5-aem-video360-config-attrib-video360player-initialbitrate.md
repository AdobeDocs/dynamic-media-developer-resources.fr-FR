---
description: Attribut de configuration de la visionneuse Video360.
solution: Experience Manager
title: Video360Player.initialbitrate
feature: Dynamic Media Classic,Visionneuses,SDK/API,vidéo 360 VR
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Attribut de configuration de la visionneuse Video360.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Définit le débit vidéo (en Kbits par seconde ou en Kbits/s) utilisé pour la lecture initiale de la vidéo sur un poste de travail. </p> <p>Si cette valeur de débit binaire n’existe pas dans la visionneuse de vidéos adaptative, le lecteur vidéo commence par la vidéo dont le débit binaire inférieur suivant. </p> <p>S’il est défini sur <span class="codeph"> 0</span>, le lecteur vidéo commence à partir du débit le plus faible possible. </p> <p>Applicable uniquement aux systèmes qui ne prennent pas en charge la vidéo HTML5 HLS en mode natif (navigateurs Firefox, Chrome et Internet Explorer 11 sous Windows 10, par exemple) et lorsque le mode de lecture est défini sur auto. </p> </td> 
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
