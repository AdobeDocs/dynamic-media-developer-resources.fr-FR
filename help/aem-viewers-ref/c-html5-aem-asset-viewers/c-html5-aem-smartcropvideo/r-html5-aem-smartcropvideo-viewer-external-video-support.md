---
title: Prise en charge vidéo externe
description: La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou de Adobe Experience Manager - Dynamic Media.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Prise en charge vidéo externe{#external-video-support}

La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou de Adobe Experience Manager - Dynamic Media.

Les formats pris en charge pour la vidéo externe sont MP4 au format H.264 ou le manifeste M3U8 pour le flux HLS.

La visionneuse peut utiliser une vidéo Dynamic Media Classic ou Experience Manager - Dynamic Media, ou une vidéo externe. Si la visionneuse commence par une vidéo Dynamic Media Classic/Dynamic Media et que vous l’utilisez avec ce type de ressource, il n’est pas possible de charger une vidéo externe dans cette visionneuse à l’aide de [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). Et vice versa : si la visionneuse a été initialement chargée avec une vidéo externe, elle doit continuer à fonctionner uniquement avec des vidéos externes.

Lorsque vous utilisez une vidéo externe, la visionneuse ignore la valeur du modificateur de lecture et détecte le type de lecture à partir de l’extension vidéo externe. Si l’URL de la vidéo externe se termine par `.M3U8` la visionneuse utilise la lecture HLS, sinon la lecture progressive est utilisée.
