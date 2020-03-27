---
description: Attribut de configuration pour le lecteur vidéo360.
seo-description: Attribut de configuration pour le lecteur vidéo360.
seo-title: Video360Player.ssl
solution: Experience Manager
title: Video360Player.ssl
topic: Dynamic media
uuid: 00c8295c-cc41-489c-a444-ba9189426a20
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video360Player.ssl{#video-player-ssl}

Attribut de configuration pour le lecteur vidéo360.

>[!NOTE]
>
>Cet attribut de configuration s’applique uniquement à AEM 6.2 avec l’installation de [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) et à AEM 6.1 avec l’installation de [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Contrôle si la vidéo est diffusée via une connexion SSL sécurisée (HTTPS) ou une connexion HTTP non sécurisée. </p> <p>Lorsqu’il est défini sur <span class="codeph"> auto</span> , le protocole  vidéo est hérité du protocole de la page Web d’incorporation. Si la page Web est chargée via HTTPS, la vidéo est également diffusée via HTTPS, et vice versa. Si la page Web est sur HTTP, la vidéo est diffusée via HTTP. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> Activé</span>, la  vidéo survient toujours sur une connexion sécurisée, quel que soit le protocole de la page Web. </p> <p>Affecte uniquement les  de vidéo publiées et est ignoré pour les  de vidéo en mode Auteur. </p> </td> 
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

Voir aussi [vidéo](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27)sécurisé.
