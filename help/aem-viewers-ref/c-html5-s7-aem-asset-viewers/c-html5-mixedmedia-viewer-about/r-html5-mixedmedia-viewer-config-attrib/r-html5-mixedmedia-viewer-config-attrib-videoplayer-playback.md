---
title: VideoPlayer.playback
description: Attribut de configuration pour la visionneuse de vidéos de médias mixtes.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
TQID: 'https://experienceleague.adobe.com/BWApI4QtEvmeQk1vNJDLtKIvrG3uO02oUlOVEGhyl2s'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

Attribut de configuration pour la visionneuse de vidéos de médias mixtes.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Définit le type de lecture utilisé par la visionneuse. Lorsque <span class="codeph"> paramètre auto</span> est défini, sur la plupart des navigateurs de bureau et tous les appareils iOS, la visionneuse utilise la vidéo en flux continu HTML5 au format HLS. Elle revient à la lecture progressive d’HTML5 sur certains systèmes tels que les anciens Internet Explorer et Android™. </p> <p>Si <span class="codeph"> progressive</span> est spécifié, la visionneuse ne s’appuie que sur la lecture HTML5 prise en charge en mode natif par les navigateurs et lit la vidéo progressivement sur tous les systèmes. </p> <p>Pour plus d’informations sur la sélection de la lecture en modes automatique et progressif, consultez le Guide d’utilisation de la visionneuse SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
