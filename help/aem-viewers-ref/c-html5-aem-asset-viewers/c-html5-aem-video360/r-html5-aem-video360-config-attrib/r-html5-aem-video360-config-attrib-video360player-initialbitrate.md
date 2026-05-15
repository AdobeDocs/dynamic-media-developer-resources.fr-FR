---
title: Video360Player.initialbitrate
description: Attribut de configuration pour la visionneuse Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
TQID: 'https://experienceleague.adobe.com/WQzO6KrubdHhlXoJgOmHxwsGXvSbPSbyJNVo-VnOz0k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 2%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Attribut de configuration pour la visionneuse Video360.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valeur </span> </p> </td> 
   <td colname="col2"> <p> Définit le débit vidéo (en kilobits par seconde ou kbit/s) utilisé pour la lecture initiale d’une vidéo sur un bureau. </p> <p>Si cette valeur de débit n’existe pas dans la visionneuse de vidéos adaptative, le lecteur vidéo commence par la vidéo qui a le débit le plus faible suivant. </p> <p>S’il est défini sur <span class="codeph"> 0</span>, le lecteur vidéo démarre à partir du débit le plus faible possible. </p> <p>Applicable uniquement aux systèmes qui ne prennent pas en charge nativement la vidéo HTML5 HLS (tels que les navigateurs Firefox, Chrome et Internet Explorer 11 sur Windows 10) et lorsque le mode de lecture est défini sur auto. </p> </td> 
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
