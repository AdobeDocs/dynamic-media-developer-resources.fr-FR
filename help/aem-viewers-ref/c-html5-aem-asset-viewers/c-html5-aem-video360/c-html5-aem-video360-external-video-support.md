---
description: Le lecteur prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou de AEM Dynamic Media.
solution: Experience Manager
title: Prise en charge vidéo externe
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Prise en charge vidéo externe{#external-video-support}

Le lecteur prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou de AEM Dynamic Media.

Les formats pris en charge pour la vidéo externe sont MP4 au format H.264 ou manifeste M3U8 pour le flux HLS.

La visionneuse peut travailler soit sur une vidéo Dynamic Media Classic, soit AEM Dynamic Media, soit sur une vidéo externe. Si la visionneuse début avec la vidéo Dynamic Media Classic/AEM Dynamic Media, elle doit être utilisée avec ce type de fichier à partir de maintenant. Il n’est pas possible de charger une vidéo externe dans cette visionneuse à l’aide de la méthode [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) et vice versa. En d’autres termes, si la visionneuse a été initialement chargée avec une vidéo externe, elle continue de fonctionner avec des vidéos externes uniquement.

Lorsque vous travaillez avec une vidéo externe, la visionneuse ignore la valeur de tout modificateur de lecture et détecte le type de lecture à partir de l’extension vidéo externe. Si l’URL de la vidéo externe se termine par `.m3u8`, la visionneuse utilise la lecture HLS ; sinon, la lecture progressive est utilisée.
