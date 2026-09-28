---
title: SmartCropVideoPlayer.preload
description: Indique si la visionneuse commence à charger le contenu vidéo avant le début de la lecture.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7a83a02e-7b75-4f15-b8c1-aa7b64e6d3bd
TQID: 'https://experienceleague.adobe.com/9TANzGaa20Kq6XdLTQRQxtxUrym6Gr6VOqdwLNS3Gps'
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
source-wordcount: '121'
ht-degree: 4%
---
# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

Indique si la visionneuse commence à charger le contenu vidéo avant le début de la lecture.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Si la valeur est définie sur <span class="codeph"> 1, </span> la vidéo commence à être téléchargée juste après la définition de la ressource. Dans le cas contraire, le préchargement ne commence qu’une fois la lecture lancée par l’utilisateur final ou un appel API. </p> <p>Si elle est définie sur <span class="codeph"> 0 </span> certaines fonctionnalités peuvent ne pas fonctionner jusqu’à ce que la lecture redémarre ; en particulier, l’opération de recherche ne met pas à jour l’image vidéo. Si l’image d’affiche est désactivée, la visionneuse s’affiche comme une zone vide au lieu de la première image vidéo. </p> <p>La désactivation du préchargement vidéo peut être ignorée sur certaines versions des navigateurs Internet Explorer 11 et Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
