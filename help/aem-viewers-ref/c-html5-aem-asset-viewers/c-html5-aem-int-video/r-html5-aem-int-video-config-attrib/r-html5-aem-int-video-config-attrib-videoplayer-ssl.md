---
title: VideoPlayer.ssl
description: Attribut de configuration de la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 16e17e2f-be98-4a5a-ba5e-5d18e7f76fa4
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# VideoPlayer.ssl{#videoplayer-ssl}

Attribut de configuration de la visionneuse de vidéos interactives.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Contrôle si la vidéo est diffusée via une connexion SSL sécurisée (HTTPS) ou une connexion non sécurisée (HTTP). </p> <p>Lorsqu’il est défini sur <span class="codeph"> auto</span>, le protocole de diffusion vidéo est hérité du protocole de la page web d’incorporation. Si la page web est chargée via HTTPS, la vidéo est également diffusée via HTTPS, et inversement. Si la page web est sur HTTP, la vidéo est diffusée sur HTTP. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> sur </span>, la diffusion vidéo s’effectue toujours sur une connexion sécurisée sans tenir compte du protocole de la page web. </p> <p>Concerne uniquement la diffusion vidéo publiée et est ignoré pour la prévisualisation vidéo en mode création. </p> </td> 
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

Voir aussi [Diffusion vidéo sécurisée](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27).
