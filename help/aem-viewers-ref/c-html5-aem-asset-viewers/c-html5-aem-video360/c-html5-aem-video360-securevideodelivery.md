---
title: Diffusion vidéo HTTPS
description: Diffusion vidéo HTTPS
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 79f7e356-55d1-46e1-b85a-2e73633c9404
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Diffusion vidéo HTTPS{#https-video-delivery}

<!-- >[!NOTE]
>
>HTTP Secure Video Delivery applies only to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Si la visionneuse fonctionne en configuration comme indiqué au début de cette section, la diffusion vidéo publiée peut avoir lieu en mode HTTPS (sécurisé) et HTTP (non sécurisé). Dans une configuration par défaut, le protocole de diffusion vidéo suit strictement le protocole de diffusion de la page web d’intégration. Cependant, il est possible de forcer la diffusion vidéo HTTPS sans tenir compte du protocole utilisé par l’incorporation de la page web à l’aide de l’attribut de configuration [Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md) . (L’aperçu vidéo en mode création est toujours diffusé en toute sécurité via HTTPS.)

Selon la méthode de publication de vidéo Dynamic Media que vous utilisez dans Adobe Experience Manager, l’attribut de configuration `Video360Player.ssl` est appliqué différemment, comme illustré ci-dessous :

* Si vous publiez une vidéo Dynamic Media avec une URL, vous ajoutez `Video360Player.ssl` à l’URL. Par exemple, pour forcer la diffusion sécurisée de vidéos, vous ajoutez `&Video360Player.ssl=on` à la fin de l’exemple d’URL de visionneuse suivant :

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
  ```

  Voir aussi [Liaison d’URL à une application web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Si vous publiez une vidéo Dynamic Media avec du code incorporé, vous ajoutez `Video360Player.ssl` à la liste d’autres paramètres de configuration de la visionneuse dans le fragment de code incorporé. Par exemple, pour forcer la diffusion vidéo HTTPS, vous ajoutez `&Video360Player.ssl=on` comme dans l’exemple suivant :

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

  Voir aussi [Incorporation de la vidéo dans une page web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)
