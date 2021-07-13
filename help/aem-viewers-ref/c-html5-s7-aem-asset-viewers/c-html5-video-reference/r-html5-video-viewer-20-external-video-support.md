---
description: La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou d’AEM Dynamic Media.
solution: Experience Manager
title: Prise en charge vidéo externe
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéo
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Prise en charge vidéo externe{#external-video-support}

La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou d’AEM Dynamic Media.

Les formats pris en charge pour la vidéo externe sont MP4 au format H.264 ou manifeste M3U8 pour le flux HLS.

La visionneuse peut utiliser une vidéo Dynamic Media Classic ou Dynamic Media AEM ou avec une vidéo externe. Si la visionneuse commence par la vidéo Dynamic Media Classic/Dynamic Media, utilisez-la avec ce type de ressource. Il n’est pas possible de charger une vidéo externe dans cette visionneuse à l’aide de la méthode [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). Et vice versa : si la visionneuse a été initialement chargée avec de la vidéo externe, elle doit continuer à fonctionner avec des vidéos externes uniquement.

Lorsque vous utilisez une vidéo externe, la visionneuse ignore la valeur du modificateur de lecture et détecte le type de lecture à partir de l’extension vidéo externe. Si l’URL de vidéo externe se termine par .m3u8, la visionneuse utilise la lecture HLS, sinon la lecture progressive est utilisée.
