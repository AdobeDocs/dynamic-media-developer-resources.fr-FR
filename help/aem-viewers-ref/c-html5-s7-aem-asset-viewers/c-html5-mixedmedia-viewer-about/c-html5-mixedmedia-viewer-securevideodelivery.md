---
description: 'null'
seo-description: 'null'
seo-title: 'vidéo HTTPS '
solution: Experience Manager
title: 'vidéo HTTPS '
topic: Dynamic media
uuid: 7f8c1fe6-b464-4d80-9ffe-a36081825d49
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365

---


# vidéo HTTPS{#https-video-delivery}

>[!NOTE]
>
>Le vidéo sécurisé s’applique uniquement à AEM 6.2 avec l’installation de [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) et à AEM 6.1 avec l’installation de [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Si le lecteur fonctionne dans la configuration décrite au début de cette section, les  de vidéo publiées peuvent se produire en mode HTTPS (sécurisé) et HTTP (non sécurisé). Dans une configuration par défaut, le protocole  vidéo suit strictement le protocole de la page Web d’intégration. Cependant, il est possible de forcer les vidéo HTTPS sans tenir compte du protocole utilisé en incorporant la page Web à l’aide de l’attribut de configuration [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) . (Notez que les  vidéo en mode Auteur sont toujours diffusées en toute sécurité sur HTTPS.)

Selon la méthode de publication de vidéo de média dynamique utilisée dans AEM, l’attribut `VideoPlayer.ssl` de configuration est appliqué différemment, comme illustré ci-dessous :

* Si vous publiez une vidéo Contenu multimédia dynamique avec une URL, vous ajoutez `VideoPlayer.ssl` à l’URL. Par exemple, pour forcer des  vidéo sécurisées, vous ajoutez `&VideoPlayer.ssl=on` à la fin de l’exemple d’URL de la visionneuse suivante :

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   See also [(Linking URLs to your Web Application](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Si vous publiez une vidéo Contenu multimédia dynamique avec du code incorporé, vous ajoutez `VideoPlayer.ssl` au d’autres paramètres de configuration de la visionneuse dans le fragment de code incorporé. Par exemple, pour forcer le vidéo HTTPS, vous ajoutez `&VideoPlayer.ssl=on` comme dans l’exemple suivant :

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

   See also [(Embedding the Video on a Web Page](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

