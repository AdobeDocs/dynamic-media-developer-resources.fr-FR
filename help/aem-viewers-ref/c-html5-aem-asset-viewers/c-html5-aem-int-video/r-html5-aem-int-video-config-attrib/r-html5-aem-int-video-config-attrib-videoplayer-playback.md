---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 2576f433-b9c2-4da1-9a51-f66b71d5df99
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

Attribut de configuration pour la visionneuse de vidéos interactive.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Définit le type de lecture utilisé par la visionneuse. </p> <p>Lorsque <span class="codeph"> auto</span> est défini, dans la plupart des navigateurs de bureau et sur tous les périphériques iOS, la visionneuse utilise la vidéo en flux continu HTML5 au format HLS et revient à la lecture HTML5 progressive sur certains systèmes tels que l’ancien Internet Explorer et Android. </p> <p>Lorsque <span class="codeph"> progressive</span> est défini, la visionneuse ne s’appuie que sur la lecture HTML5, prise en charge en mode natif par les navigateurs, et lit la vidéo progressivement sur tous les systèmes. </p> <p>Pour plus d’informations sur la sélection de lecture en modes natifs <span class="codeph"> auto</span> et <span class="codeph"> progressive</span>, consultez le Guide de l’utilisateur du kit de développement de visionneuses HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
