---
description: Attribut de configuration pour la visionneuse de vidéos.
solution: Experience Manager
title: VideoPlayer.ssl
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: f7d832f3-e9b1-4161-a572-851e538bb245
source-git-commit: c58199c5884c368e92e50fe0ef9d6ad523e36266
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# VideoPlayer.ssl{#videoplayer-ssl}

Attribut de configuration pour la visionneuse de vidéos.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Contrôle si la vidéo est diffusée via une connexion SSL sécurisée (HTTPS) ou une connexion non sécurisée (HTTP). </p> <p>Lorsqu’il est défini sur <span class="codeph"> auto</span>, le protocole de diffusion vidéo est hérité du protocole de la page web d’intégration. Si la page web est chargée via HTTPS, la vidéo est également diffusée via HTTPS, et vice versa. Si la page web est sur HTTP, la vidéo est diffusée sur HTTP. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> sur</span>, la diffusion vidéo s’effectue toujours sur une connexion sécurisée sans tenir compte du protocole de la page web. </p> <p>Concerne uniquement la diffusion vidéo publiée et est ignoré pour la prévisualisation vidéo en mode création. </p> </td> 
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
