---
description: Attribut de configuration pour la visionneuse Video360.
solution: Experience Manager
title: Video360Player.ssl
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
exl-id: 44efa378-c911-4449-8a10-61212d4392c6
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 4%

---

# Video360Player.ssl{#video-player-ssl}

Attribut de configuration pour la visionneuse Video360.

>[!NOTE]
>
>Cet attribut de configuration s&#39;applique uniquement à AEM 6.2 avec l&#39;installation de [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) et à AEM 6.1 avec l&#39;installation de [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Contrôle si la vidéo est diffusée via une connexion SSL sécurisée (HTTPS) ou une connexion HTTP non sécurisée. </p> <p>Lorsqu’il est défini sur <span class="codeph"> auto</span>, le protocole de diffusion vidéo est hérité du protocole de la page Web incorporée. Si la page Web est chargée via HTTPS, la vidéo est également diffusée via HTTPS, et vice versa. Si la page Web est sur HTTP, la vidéo est diffusée via HTTP. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> sur </span>, la diffusion vidéo survient toujours sur une connexion sécurisée sans tenir compte du protocole de la page Web. </p> <p>Affecte uniquement la diffusion vidéo publiée et est ignorée pour la prévisualisation vidéo en mode Auteur. </p> </td> 
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

Voir aussi [Diffusion vidéo sécurisée](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27).
