---
title: Prise en charge vidéo externe
description: La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Prise en charge vidéo externe{#external-video-support}

La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou Adobe Experience Manager - Dynamic Media.

Les formats pris en charge pour la vidéo externe sont MP4 au format H.264 ou manifeste M3U8 pour le flux HLS.

La visionneuse peut fonctionner avec une vidéo Dynamic Media Classic ou Experience Manager - Dynamic Media ou avec une vidéo externe. Si la visionneuse commence par une vidéo Dynamic Media Classic/Dynamic Media, utilisez-la avec ce type de ressource. Il n’est pas possible de charger une vidéo externe dans cette visionneuse à l’aide de [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) . Et vice versa : si la visionneuse a été initialement chargée avec de la vidéo externe, elle doit continuer à fonctionner avec des vidéos externes uniquement.

Lorsque vous utilisez une vidéo externe, la visionneuse ignore la valeur du modificateur de lecture et détecte le type de lecture à partir de l’extension vidéo externe. Si l’URL de la vidéo externe se termine par `.M3U8` la visionneuse utilise la lecture HLS ; dans le cas contraire, la lecture progressive est utilisée.
