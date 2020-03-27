---
description: Attribut de configuration pour la visionneuse de vidéos de supports variés.
seo-description: Attribut de configuration pour la visionneuse de vidéos de supports variés.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.playback{#videoplayer-playback}

Attribut de configuration pour la visionneuse de vidéos de supports variés.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Définit le type de lecture utilisé par la visionneuse. Lorsque l’option <span class="codeph"> auto</span> est définie, sur la plupart des navigateurs de bureau et sur tous les périphériques iOS, le lecteur utilise la vidéo en flux continu HTML5 au format HLS. Il revient à la lecture HTML5 progressive sur certains systèmes tels qu’Internet Explorer et Android plus anciens. </p> <p>Si <span class="codeph"> progressif</span> est spécifié, le lecteur ne s’appuie que sur la lecture HTML5 en tant que prise en charge native par les navigateurs et lit la vidéo progressivement sur tous les systèmes. </p> <p>Pour plus d’informations sur la sélection de la lecture en mode automatique et progressif, consultez le Guide de l’utilisateur du SDK du lecteur. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
