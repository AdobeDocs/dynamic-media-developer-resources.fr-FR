---
description: La bibliothèque d’images réactives est un module JavaScript qui ajuste dynamiquement la qualité des images diffusées à partir de Dynamic Media et incorporées dans des pages web réactives. En outre, il offre une qualité d’image améliorée sur les périphériques dotés d’écrans haute densité. La bibliothèque peut également générer de manière réactive les résultats à partir du recadrage intelligent et de l’échantillon intelligent.
solution: Experience Manager
title: À propos de la bibliothèque d’images réactives
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# À propos de la bibliothèque d’images réactives{#about-responsive-image-library}

La bibliothèque d’images réactives est un module JavaScript qui ajuste dynamiquement la qualité des images diffusées à partir de Dynamic Media et incorporées dans des pages web réactives. En outre, il offre une qualité d’image améliorée sur les périphériques dotés d’écrans haute densité. La bibliothèque peut également générer de manière réactive les résultats à partir du recadrage intelligent et de l’échantillon intelligent.

## URL de démonstration {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Le cas d’utilisation le plus simple de la bibliothèque d’images réactives consiste à définir une liste de valeurs de point d’arrêt pour la largeur de l’image. Cette liste permet de s’assurer que le rendu approprié est chargé et affiché lorsqu’une image est redimensionnée en raison de la mise en page d’une page web qui change à partir du redimensionnement de la fenêtre du navigateur par un utilisateur ou de la modification de l’orientation de l’appareil. La bibliothèque surveille en permanence la taille de l’image à l’écran et, chaque fois qu’une nouvelle largeur de point d’arrêt est atteinte, elle récupère un nouveau rendu d’image à partir de Dynamic Media.

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>URL de démonstration </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>Voici un exemple simple où l’image réactive se trouve dans un conteneur qui prend 50 % de la largeur de la page web. Chaque fois que la fenêtre du navigateur est redimensionnée, la largeur du conteneur change. Lorsque la largeur de l’image atteint l’un des points d’arrêt configurés (définis à 200, 400, 600 et 800 pixels à des fins d’illustration), un nouveau rendu est téléchargé et affiché. L’objectif est d’éviter de charger des images volumineuses superflues et d’économiser la bande passante du réseau. </p> <p>Cliquez sur l’URL pour ouvrir la page web, redimensionner la fenêtre du navigateur et contrôler le trafic réseau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>L’exemple de Bootstrap suivant illustre le même cas d’utilisation dans une page web. Selon Bootstrap CSS, la cellule de disposition à laquelle l’image réactive est ajoutée peut avoir l’une des largeurs suivantes : 360, 720 et 940 pixels. Ces valeurs sont exactement ce qui est transmis en tant que points d’arrêt à la bibliothèque d’images réactives. Ainsi, Dynamic Media s’assure que la bande passante réseau du client est utilisée efficacement. De plus, il garantit également que l’image est affichée à la taille exacte nécessaire, compte tenu de la mise en page web actuelle, sans artefacts visuels lors de la mise à l’échelle du navigateur côté client. </p> <p>Cliquez sur l’URL pour ouvrir la page web, redimensionnez la fenêtre du navigateur afin d’atteindre différents points d’arrêt de mise en page et surveiller le trafic réseau. </p> <p>Les cas d’utilisation plus avancés incluent l’association de différents paramètres d’image prédéfinis ou commandes de diffusion d’images, ou les deux, à des valeurs de point d’arrêt différentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>Dans l’exemple suivant, des paramètres d’image prédéfinis de qualité et de format d’image différents pour différentes tailles de points d’arrêt sont utilisés. Pour un petit point d’arrêt, un paramètre prédéfini de faible qualité est appliqué, ce qui force le serveur d’images à renvoyer l’image GIF compressée à six couleurs uniquement. Un point d’arrêt moyen utilise un paramètre d’image prédéfini configuré pour le format JPEG avec une compression élevée. Le point d’arrêt le plus grand est associé à un paramètre d’image prédéfini de haute qualité à l’aide d’un fichier PNG sans perte. Cette méthode garantit que les images de haute qualité sont diffusées vers ces appareils, en partant du principe que les appareils dotés d’écrans plus grands disposent d’une bande passante et d’une puissance de traitement plus importantes. </p> <p>Cliquez sur l’URL pour ouvrir la page web, redimensionnez la fenêtre du navigateur web de la plus grande à la plus petite, et notez la dégradation de la qualité de l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Outre les paramètres d’image prédéfinis, il est possible d’associer des commandes de diffusion d’images spécifiques à des points d’arrêt. L’exemple suivant montre comment recadrer progressivement l’image de bannière dans la région concernée lorsque la taille de l’image à l’écran devient plus petite. Ici, le point d’arrêt le plus grand ne comporte aucune commande de diffusion d’images. L’image de bannière est donc entièrement visible. Au point d’arrêt moyen, le recadrage est modéré, ce qui rend visible uniquement le coureur avec le texte "En cours d’exécution". Plus de recadrage est appliqué au petit point d’arrêt, de sorte que seul le produit s’affiche. </p> <p>Cliquez sur l’URL pour ouvrir la page web et redimensionner la fenêtre de votre navigateur. Remarquez comment l’image se recadre progressivement lorsque vous passez d’une taille plus grande à une taille plus petite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>Vous pouvez également utiliser des commandes de diffusion d’images avec des modèles de diffusion d’images pour contrôler certains paramètres de modèle en fonction de la taille de l’image. Dans l’exemple suivant, un modèle de serveur d’images est utilisé, où la taille de police de la superposition de texte est paramétrée à l’aide du paramètre <span class="codeph"> $fontsize </span> . L’image réactive est configurée de manière à utiliser une taille de police plus grande pour les images plus petites afin de s’assurer que le texte reste toujours lisible : </p> </td> 
  </tr> 
 </tbody> 
</table>

## Configuration système requise {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Matériel et logiciels du serveur**

* Dynamic Media Image Serving 6.0.1 ou version ultérieure.

**Configuration requise du navigateur client**

* Microsoft® Windows® 7 ou version ultérieure ; macOS X 10.8 ou version ultérieure.
* Firefox 23, Safari 6, Chrome 29, IE 9 ou version ultérieure.
* iOS 6 ou version ultérieure.
* Certifié sur iPhone3GS ou version ultérieure et iPad2 ou version ultérieure (navigateurs natifs uniquement).
* Android™ OS 2.3 ou version ultérieure.
* Internet Explorer sur les appareils mobiles n’est actuellement pas pris en charge.
