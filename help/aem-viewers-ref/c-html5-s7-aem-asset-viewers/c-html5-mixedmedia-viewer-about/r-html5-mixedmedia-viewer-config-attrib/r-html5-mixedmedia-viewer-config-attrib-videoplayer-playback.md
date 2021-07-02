---
description: Attribut de configuration de la visionneuse de vidéos de supports variés.
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

Attribut de configuration de la visionneuse de vidéos de supports variés.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressif</span> </p> </td> 
   <td colname="col2"> <p> Définit le type de lecture utilisé par la visionneuse. Lorsque la variable <span class="codeph"> auto</span> est définie, sur la plupart des navigateurs de bureau et sur tous les appareils iOS, la visionneuse utilise la vidéo en flux continu HTML5 au format HLS. Il revient à la lecture HTML5 progressive sur certains systèmes tels qu’Internet Explorer et Android plus anciens. </p> <p>Si <span class="codeph"> progressif</span> est spécifié, la visionneuse ne s’appuie que sur la lecture HTML5 comme prise en charge en mode natif par les navigateurs et lit la vidéo progressivement sur tous les systèmes. </p> <p>Pour plus d’informations sur la sélection de la lecture en modes automatique et progressif, consultez le Guide de l’utilisateur du SDK de la visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
