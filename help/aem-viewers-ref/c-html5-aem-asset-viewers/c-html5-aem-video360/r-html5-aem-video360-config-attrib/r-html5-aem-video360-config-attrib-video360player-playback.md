---
title: Video360Player.playback
description: Attribut de configuration de la visionneuse Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 1%

---

# Video360Player.playback{#video-player-playback}

Attribut de configuration de la visionneuse Video360.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressif</span> </p> </td> 
   <td colname="col2"> <p> Définit le type de lecture utilisé par la visionneuse. </p> <p>Lorsque <span class="codeph"> auto</span> est défini, dans la plupart des navigateurs de bureau et tous les appareils iOS, la visionneuse utilise la vidéo en flux continu HTML5 au format HLS. Et il revient à la lecture progressive d’HTML5 sur certains systèmes comme Internet Explorer et Android™ plus anciens. </p> <p>Lorsque <span class="codeph"> progressif</span> est défini, la visionneuse ne s’appuie que sur la lecture HTML5 comme prise en charge en mode natif par les navigateurs et lit la vidéo progressivement sur tous les systèmes. </p> <p>Pour plus d’informations sur la sélection de la lecture dans les modes natifs <span class="codeph"> auto</span> et <span class="codeph"> progressif</span>, consultez le Guide de l’utilisateur du SDK des visionneuses HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif. Ignoré lorsque la visionneuse fonctionne avec une vidéo externe.

Pour plus d’informations, voir [Prise en charge de vidéos externes](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) .

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
