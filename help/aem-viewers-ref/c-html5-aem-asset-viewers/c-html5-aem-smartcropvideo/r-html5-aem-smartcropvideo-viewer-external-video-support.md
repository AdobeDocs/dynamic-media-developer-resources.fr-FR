---
title: Prise en charge vidéo externe
description: La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Prise en charge vidéo externe{#external-video-support}

La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou Adobe Experience Manager - Dynamic Media.

Les formats pris en charge pour la vidéo externe sont MP4 au format H.264 ou manifeste M3U8 pour le flux HLS.

La visionneuse peut fonctionner Dynamic Media vidéo classique ou Experience Manager - Dynamic Media ou avec une vidéo externe. Si la visionneuse commence par Dynamic Media vidéo Classic/Dynamic Media, utilisez-la avec ce type de ressource à l’avenir, il n’est pas possible de charger une vidéo externe dans cette visionneuse à l’aide [`setVideo`] de
(.. /.. /c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). Et vice versa : si le spectateur a été initialement chargé avec une vidéo externe, il devrait continuer à fonctionner uniquement avec des vidéos externes.

Lorsqu’il travaille avec une vidéo externe, le spectateur ignore la valeur du modificateur de lecture et détecte le type de lecture de l’extension vidéo externe. Si l’URL vidéo externe se termine par `.M3U8` la lecture HLS, la lecture progressive est utilisée.
