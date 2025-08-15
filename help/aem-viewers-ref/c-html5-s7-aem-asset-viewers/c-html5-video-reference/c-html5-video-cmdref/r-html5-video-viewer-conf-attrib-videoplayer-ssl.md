---
title: VideoPlayer.ssl
description: Attribut de configuration de la visionneuse de vidéos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: f7d832f3-e9b1-4161-a572-851e538bb245
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# VideoPlayer.ssl{#videoplayer-ssl}

Attribut de configuration de la visionneuse de vidéos.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|activé</span> </p> </td> 
   <td colname="col2"> <p> Contrôle si la vidéo est diffusée via une connexion SSL sécurisée (HTTPS) ou une connexion non sécurisée (HTTP). </p> <p>Lorsque vous définissez ce paramètre sur <span class="codeph"> auto</span> le protocole de diffusion vidéo est hérité du protocole de la page web d’incorporation. Si la page web est chargée via HTTPS, la vidéo est également diffusée via HTTPS, et inversement. Si la page web se trouve sur HTTP, la vidéo est diffusée sur HTTP. </p> <p>Lorsque ce paramètre est défini sur <span class="codeph"> activé</span> la diffusion vidéo s’effectue toujours via une connexion sécurisée, quel que soit le protocole de la page web. </p> <p>Affecte uniquement la diffusion vidéo publiée et est ignorée pour la prévisualisation vidéo en mode création. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

Voir aussi [Diffusion vidéo sécurisée](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff).
