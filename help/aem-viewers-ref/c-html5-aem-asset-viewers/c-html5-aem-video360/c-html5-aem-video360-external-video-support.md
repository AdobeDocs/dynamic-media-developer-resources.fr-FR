---
description: Le lecteur prend en charge la lecture de vidéos hébergées en dehors de SPS ou d’AEM Dynamic Media.
seo-description: Le lecteur prend en charge la lecture de vidéos hébergées en dehors de SPS ou d’AEM Dynamic Media.
seo-title: Prise en charge vidéo externe
solution: Experience Manager
title: Prise en charge vidéo externe
topic: Dynamic media
uuid: 2e9f1c54-627f-4462-ae85-8a5ca1d09762
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge vidéo externe{#external-video-support}

Le lecteur prend en charge la lecture de vidéos hébergées en dehors de SPS ou d’AEM Dynamic Media.

Les formats pris en charge pour la vidéo externe sont MP4 au format H.264 ou manifeste M3U8 pour le flux HLS.

La visionneuse peut travailler sur une vidéo Dynamic Media Classic ou AEM Dynamic Media ou sur une vidéo externe. Si le de la visionneuse  avec la vidéo Dynamic Media Classic/AEM Dynamic Media, il doit être utilisé avec un tel type de ressource. Il n’est pas possible de charger une vidéo externe dans cette visionneuse à l’aide de la méthode [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) et vice versa. En d’autres termes, si la visionneuse a été initialement chargée avec une vidéo externe, elle continue de fonctionner avec des vidéos externes uniquement.

Lorsque vous travaillez avec une vidéo externe, la visionneuse ignore la valeur de tout modificateur de lecture et détecte le type de lecture à partir de l’extension vidéo externe. Si l’URL de vidéo externe se termine par `.m3u8`, le lecteur utilise la lecture HLS ; sinon, la lecture progressive est utilisée.
