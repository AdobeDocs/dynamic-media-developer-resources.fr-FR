---
description: Diffusion vidéo HTTPS
solution: Experience Manager
title: Diffusion vidéo HTTPS
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: f9651405-ebc6-4b1f-8fb6-031d0b295083
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Diffusion vidéo HTTPS{#https-video-delivery}

>[!NOTE]
>
>La diffusion vidéo sécurisée s’applique uniquement à AEM 6.2 avec l’installation du [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) et à AEM 6.1 avec l’installation du [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Si la visionneuse fonctionne comme indiqué au début de cette section, la diffusion vidéo publiée peut avoir lieu en mode HTTPS (sécurisé) et HTTP (non sécurisé). Dans une configuration par défaut, le protocole de diffusion vidéo suit strictement le protocole de diffusion de la page web d’intégration. Cependant, il est possible de forcer la diffusion vidéo HTTPS sans tenir compte du protocole utilisé en incorporant la page web à l’aide de l’attribut de configuration [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) . (Notez que l’aperçu vidéo en mode création est toujours diffusé en toute sécurité via HTTPS.)

Selon la méthode de publication de vidéo Dynamic Media que vous utilisez dans AEM, l’attribut de configuration `VideoPlayer.ssl` est appliqué différemment, comme illustré ci-dessous :

* Si vous publiez une vidéo Dynamic Media avec une URL, vous ajoutez `VideoPlayer.ssl` à l’URL. Par exemple, pour forcer la diffusion sécurisée de vidéos, vous ajoutez `&VideoPlayer.ssl=on` à la fin de l’exemple d’URL de visionneuse suivant :

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   Voir aussi [(Liaison d’URL à une application web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Si vous publiez une vidéo Dynamic Media avec du code incorporé, vous ajoutez `VideoPlayer.ssl` à la liste des autres paramètres de configuration de la visionneuse dans le fragment de code incorporé. Par exemple, pour forcer la diffusion vidéo HTTPS, vous ajoutez `&VideoPlayer.ssl=on` comme dans l’exemple suivant :

   ```
   <style type="text/css"> 
    #s7mixedmedia_div.s7mixedmediaviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/MixedMediaViewer.js"></script> 
   <div id="s7mixedmedia_div"></div> 
   <script type="text/javascript"> 
    var s7mixedmediaviewer = new s7viewers.MixedMediaViewer({ 
     "containerId" : "s7mixedmedia_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/MixedMedia_light", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "asset" : "/content/dam/Geometrixx-Outdoors-New-Launch/backpack/backpack_mixed_media" } 
    }).init(); 
   </script>
   ```

   Voir aussi [(Incorporation de la vidéo dans une page web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
