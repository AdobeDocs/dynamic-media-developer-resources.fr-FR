---
title: Prise en charge vidéo externe
description: La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou de Adobe Experience Manager - Dynamic Media.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
TQID: 'https://experienceleague.adobe.com/nLVjtwe8hj5YpMX6M1GKt1Fx-tZK2Qxe1kdWcK8BQPw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%
---
# Prise en charge vidéo externe{#external-video-support}

La visionneuse prend en charge la lecture de vidéos hébergées en dehors de Dynamic Media Classic ou de Adobe Experience Manager - Dynamic Media.

Les formats pris en charge pour la vidéo externe sont MP4 au format H.264 ou le manifeste M3U8 pour le flux HLS.

La visionneuse peut utiliser une vidéo Dynamic Media Classic ou Experience Manager - Dynamic Media, ou une vidéo externe. Si la visionneuse commence par une vidéo Dynamic Media Classic/Dynamic Media et que vous l’utilisez avec ce type de ressource, il n’est pas possible de charger une vidéo externe dans cette visionneuse à l’aide de [`setVideo`]
(#reference-85d3422d6ce64a36ac74827120b5a17c). Et vice versa : si la visionneuse a été initialement chargée avec une vidéo externe, elle doit continuer à fonctionner uniquement avec des vidéos externes.

Lorsque vous utilisez une vidéo externe, la visionneuse ignore la valeur du modificateur de lecture et détecte le type de lecture à partir de l’extension vidéo externe. Si l’URL de la vidéo externe se termine par `.M3U8` la visionneuse utilise la lecture HLS, sinon la lecture progressive est utilisée.
