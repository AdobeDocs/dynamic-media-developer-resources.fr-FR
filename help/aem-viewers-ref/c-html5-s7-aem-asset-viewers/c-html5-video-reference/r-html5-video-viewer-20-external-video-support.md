---
description: Le lecteur prend en charge la lecture de vidéos hébergées en dehors de Scene7 Publishing System ou d’AEM Dynamic Media.
seo-description: Le lecteur prend en charge la lecture de vidéos hébergées en dehors de Scene7 Publishing System ou d’AEM Dynamic Media.
seo-title: Prise en charge vidéo externe
solution: Experience Manager
title: Prise en charge vidéo externe
topic: Dynamic media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# Prise en charge vidéo externe{#external-video-support}

Le lecteur prend en charge la lecture de vidéos hébergées en dehors de Scene7 Publishing System ou d’AEM Dynamic Media.

Les formats pris en charge pour la vidéo externe sont MP4 au format H.264 ou manifeste M3U8 pour le flux HLS.

La visionneuse peut travailler sur une vidéo Scene7 ou Dynamic Media ou avec une vidéo externe. Si la visionneuse début avec la vidéo Scene7/Dynamic Media, utilisez-la avec un tel type de fichier, il n’est pas possible de charger une vidéo externe dans cette visionneuse à l’aide de la méthode [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). Et vice versa : si la visionneuse était initialement chargée avec une vidéo externe, elle ne devrait continuer à travailler qu’avec des vidéos externes.

Lorsque vous travaillez avec une vidéo externe, la visionneuse ignore la valeur du modificateur playback et détecte le type de lecture de l’extension vidéo externe. Si l’URL de vidéo externe se termine par .m3u8, le lecteur utilise la lecture HLS, sinon la lecture progressive est utilisée.
