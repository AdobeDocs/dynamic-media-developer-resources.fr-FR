---
title: Diffusion vidéo HTTP
description: Diffusion vidéo HTTP
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 33907e22-107b-4345-82bb-cad47cb7a839
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Diffusion vidéo HTTP{#http-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Si la visionneuse fonctionne dans la configuration décrite au début de cette section, la diffusion vidéo publiée peut se produire en modes HTTPS (sécurisé) et HTTP (non sécurisé). Dans une configuration par défaut, le protocole de diffusion vidéo suit strictement le protocole de diffusion de la page web d’incorporation. Cependant, il est possible de forcer la diffusion vidéo HTTPS quel que soit le protocole utilisé en incorporant la page web à l’aide de l’attribut de configuration [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). (L’aperçu vidéo en mode création est toujours diffusé en toute sécurité via HTTPS.)

Selon la méthode de publication de la vidéo Dynamic Media que vous utilisez dans Adobe Experience Manager, l’attribut de configuration `VideoPlayer.ssl` s’applique différemment, comme illustré ci-dessous :

* Si vous publiez une vidéo Dynamic Media avec une URL, vous ajoutez des `VideoPlayer.ssl` à l’URL.

<!-- For example, to force secure video delivery, you append `&VideoPlayer.ssl=on` to the end of the following viewer URL example: -->

<!--

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/VideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&VideoPlayer.ssl=on
  ```

-->

Voir aussi [Liaison d’URL à une application web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Si vous publiez une vidéo Dynamic Media avec du code intégré, vous ajoutez `VideoPlayer.ssl` à la liste des autres paramètres de configuration de la visionneuse dans le fragment de code intégré.

<!-- For example, to force HTTPS video delivery, you append `&VideoPlayer.ssl=on` as in the following example: -->

<!--

  ```
  <style type="text/css"> 
   #s7video_div.s7videoviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/VideoViewer.js"></script> 
  <div id="s7video_div"></div> 
  <script type="text/javascript"> 
   var s7videoviewer = new s7viewers.VideoViewer({ 
    "containerId" : "s7video_div", 
    "params" : {  
     "VideoPlayer.ssl" : "on", 
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

-->

Voir aussi [&#x200B; Incorporation de la vidéo dans une page web &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
