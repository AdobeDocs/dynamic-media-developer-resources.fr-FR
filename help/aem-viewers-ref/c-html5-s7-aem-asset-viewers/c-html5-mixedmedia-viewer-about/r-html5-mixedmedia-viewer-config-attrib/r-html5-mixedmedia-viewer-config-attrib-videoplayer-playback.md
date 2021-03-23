---
description: Attribut de configuration pour la visionneuse de vidéos de supports variés.
seo-description: Attribut de configuration pour la visionneuse de vidéos de supports variés.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
feature: Dynamic Media Classic, Visionneuses, SDK/API, Combiner des visionneuses de supports
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

Attribut de configuration pour la visionneuse de vidéos de supports variés.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Définit le type de lecture utilisé par la visionneuse. Lorsque <span class="codeph"> auto</span> est défini, sur la plupart des navigateurs de bureau et sur tous les périphériques iOS, la visionneuse utilise la vidéo en flux continu HTML5 au format HLS. Il revient à la lecture HTML5 progressive sur certains systèmes tels que l’ancien Internet Explorer et Android. </p> <p>Si <span class="codeph"> progressive</span> est spécifié, la visionneuse ne s’appuie que sur la lecture HTML5, prise en charge en mode natif par les navigateurs, et lit la vidéo progressivement sur tous les systèmes. </p> <p>Pour plus d’informations sur la sélection de la lecture en mode automatique et progressif, consultez le Guide de l’utilisateur du SDK de la visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
