---
description: DIFFUSION vidéo HTTP
solution: Experience Manager
title: DIFFUSION vidéo HTTP
uuid: fd02a55a-a0f1-47a2-983f-15f296d1dbb4
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---


# DIFFUSION vidéo HTTP{#http-video-delivery}

>[!NOTE]
>
>La Diffusion vidéo sécurisée s’applique uniquement à AEM 6.2 avec l’installation de [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) et à AEM 6.1 avec l’installation de [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Pour autant que la visionneuse fonctionne dans la configuration décrite au début de cette section, la diffusion vidéo publiée peut se produire en mode HTTPS (sécurisé) et HTTP (non sécurisé). Dans une configuration par défaut, le protocole de la diffusion vidéo respecte strictement le protocole de diffusion de la page Web incorporée. Cependant, il est possible de forcer la diffusion vidéo HTTPS sans tenir compte du protocole utilisé en incorporant la page Web à l’aide de l’attribut de configuration [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). (Notez que la prévisualisation vidéo en mode Auteur est toujours diffusée en toute sécurité sur HTTPS.)

Selon la méthode de publication de la vidéo Dynamic Media que vous utilisez en AEM, l’attribut de configuration `VideoPlayer.ssl` est appliqué différemment, comme illustré ci-dessous :

* Si vous publiez une vidéo Dynamic Media avec une URL, vous ajoutez `VideoPlayer.ssl` à l’URL. Par exemple, pour forcer la diffusion vidéo sécurisée, vous ajoutez `&VideoPlayer.ssl=on` à la fin de l’exemple d’URL de visionneuse suivant :

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/VideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&VideoPlayer.ssl=on
   ```

   Voir aussi [Liaison d’URL à votre Application web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Si vous publiez une vidéo Dynamic Media avec du code incorporé, vous ajoutez `VideoPlayer.ssl` à la liste des autres paramètres de configuration de la visionneuse dans le fragment de code incorporé. Par exemple, pour forcer la diffusion vidéo HTTPS, vous ajoutez `&VideoPlayer.ssl=on` comme dans l&#39;exemple suivant :

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

   Voir aussi [Incorporation de la vidéo sur une page Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).

