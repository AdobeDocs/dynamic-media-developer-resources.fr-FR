---
title: VideoPlayer.initialbitrate
description: VideoPlayer.initialbitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
TQID: 'https://experienceleague.adobe.com/43fGvsD0G1miDbzE8EQnXmTVrlCQEOP9V2r0ji83yww'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valeur <span class="varname"> </span> </span> </p> </td> 
   <td colname="col2"> <p>Définit le débit vidéo (en kilobits par seconde ou kbit/s) utilisé pour la lecture initiale de la vidéo sur les ordinateurs de bureau. </p> <p>Si cette valeur de débit n’existe pas dans la visionneuse de vidéos adaptative, le lecteur vidéo lance la vidéo qui a le débit le plus faible suivant. </p> <p>S’il est défini sur <span class="codeph"> 0 </span>, le lecteur vidéo démarre à partir du débit le plus faible possible. Applicable uniquement aux systèmes qui ne prennent pas en charge nativement la vidéo HTML5 HLS (qui sont des navigateurs Firefox, Chrome et Internet Explorer 11 sous Windows 10) et lorsque le mode de lecture est défini sur <span class="codeph"> le </span> automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
