---
title: Prise en charge vidéo externe
description: La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Prise en charge vidéo externe{#external-video-support}

La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou Adobe Experience Manager - Dynamic Media.

Les formats pris en charge pour la vidéo externe sont MP4 au format H.264 ou manifeste M3U8 pour le flux HLS.

La visionneuse peut fonctionner avec une vidéo Dynamic Media Classic ou Experience Manager - Dynamic Media ou avec une vidéo externe. Si la visionneuse commence par une vidéo Dynamic Media Classic/Dynamic Media, utilisez-la avec ce type de ressource. Il n’est pas possible de charger une vidéo externe dans cette visionneuse à l’aide de [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) . Et vice versa : si la visionneuse a été initialement chargée avec de la vidéo externe, elle doit continuer à fonctionner avec des vidéos externes uniquement.

Lorsque vous utilisez une vidéo externe, la visionneuse ignore la valeur du modificateur de lecture et détecte le type de lecture à partir de l’extension vidéo externe. Si l’URL de vidéo externe se termine par `.m3u8` la visionneuse utilise la lecture HLS ; dans le cas contraire, la lecture progressive est utilisée.
