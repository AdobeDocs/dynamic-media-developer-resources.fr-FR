---
title: Prise en charge vidéo externe
description: La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Prise en charge vidéo externe{#external-video-support}

La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou Adobe Experience Manager, Dynamic Media.

Les formats pris en charge pour la vidéo externe sont MP4 au format H.264 ou manifeste M3U8 pour le flux HLS.

La visionneuse peut utiliser une vidéo Dynamic Media Classic ou Experience Manager Dynamic Media ou une vidéo externe. Si la visionneuse commence par la vidéo Dynamic Media Classic/AEM Dynamic Media, elle doit être utilisée avec ce type de ressource. Il n’est pas possible de charger une vidéo externe dans cette visionneuse à l’aide de la méthode [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) et inversement. En d’autres termes, si la visionneuse a été initialement chargée avec une vidéo externe, elle continue de fonctionner uniquement avec des vidéos externes.

Lorsque vous utilisez une vidéo externe, la visionneuse ignore la valeur de tout modificateur de lecture et détecte le type de lecture à partir de l’extension vidéo externe. Si l’URL de la vidéo externe se termine par `.m3u8`, la visionneuse utilise la lecture HLS ; sinon, la lecture progressive est utilisée.
