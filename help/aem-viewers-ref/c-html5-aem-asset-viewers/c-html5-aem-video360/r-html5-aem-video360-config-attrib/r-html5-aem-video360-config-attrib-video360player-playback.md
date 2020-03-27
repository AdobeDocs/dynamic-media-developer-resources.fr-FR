---
description: Attribut de configuration pour le lecteur vidéo360.
seo-description: Attribut de configuration pour le lecteur vidéo360.
seo-title: Video360Player.playback
solution: Experience Manager
title: Video360Player.playback
topic: Dynamic media
uuid: ce814963-5cb8-408e-9d57-e7b7e61e0fab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.playback{#video-player-playback}

Attribut de configuration pour le lecteur vidéo360.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Définit le type de lecture utilisé par la visionneuse. </p> <p>Lorsque l’option <span class="codeph"> auto</span> est définie, dans la plupart des navigateurs de bureau et sur tous les périphériques iOS, le lecteur utilise la vidéo en flux continu HTML5 au format HLS et revient à la lecture HTML5 progressive sur certains systèmes tels qu’Internet Explorer et Android plus anciens. </p> <p>Une fois <span class="codeph"> progressive</span> définie, la visionneuse s’appuie uniquement sur la lecture HTML5 en tant que prise en charge native par les navigateurs et lit la vidéo progressivement sur tous les systèmes. </p> <p>Pour plus d’informations sur la sélection de la lecture en mode natif <span class="codeph"> automatique</span> et <span class="codeph"></span> progressif, voir le Guide de l’utilisateur du kit de développement de visionneuses HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif. Ignoré lorsque la visionneuse fonctionne avec une vidéo externe.

Voir Prise en charge [vidéo](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) externe pour plus d’informations.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
