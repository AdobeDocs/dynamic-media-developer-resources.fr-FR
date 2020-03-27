---
description: 'null'
seo-description: 'null'
seo-title: 'vidéo HTTPS '
solution: Experience Manager
title: 'vidéo HTTPS '
topic: Dynamic media
uuid: 68984ba1-2802-496a-8ad0-ba46b59514ad
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365

---


# vidéo HTTPS{#https-video-delivery}

>[!NOTE]
>
>Le vidéo sécurisé HTTP s’applique uniquement à AEM 6.2 avec l’installation de [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) et à AEM 6.1 avec l’installation de [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Si le lecteur fonctionne dans la configuration décrite au début de cette section, les  de vidéo publiées peuvent se produire en mode HTTPS (sécurisé) et HTTP (non sécurisé). Dans une configuration par défaut, le protocole  vidéo suit strictement le protocole de la page Web d’intégration. Cependant, il est possible de forcer les vidéo HTTPS sans tenir compte du protocole utilisé en incorporant la page Web à l’aide de l’attribut de configuration [Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md) . (Notez que les  vidéo en mode Auteur sont toujours diffusées en toute sécurité sur HTTPS.)

Selon la méthode de publication de vidéo de média dynamique utilisée dans AEM, l’attribut `Video360Player.ssl` de configuration est appliqué différemment, comme illustré ci-dessous :

* Si vous publiez une vidéo Contenu multimédia dynamique avec une URL, vous ajoutez `Video360Player.ssl` à l’URL. Par exemple, pour forcer des  vidéo sécurisées, vous ajoutez `&Video360Player.ssl=on` à la fin de l’exemple d’URL de la visionneuse suivante :

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   See also [Linking URLs to your Web Application](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Si vous publiez une vidéo Contenu multimédia dynamique avec du code incorporé, vous ajoutez `Video360Player.ssl` au d’autres paramètres de configuration de la visionneuse dans le fragment de code incorporé. Par exemple, pour forcer le vidéo HTTPS, vous ajoutez `&Video360Player.ssl=on` comme dans l’exemple suivant :

   ```
   <style type="text/css"> 
    #s7video_div.s7video360viewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7video360viewer = new s7viewers.Video360Viewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "Video360Player.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/Video", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
      "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
    }).init(); 
   </script>
   ```

   See also [Embedding the Video on a Web Page](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html)

