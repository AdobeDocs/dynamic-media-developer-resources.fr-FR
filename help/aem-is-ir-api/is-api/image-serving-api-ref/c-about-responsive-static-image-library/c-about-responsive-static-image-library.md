---
description: La bibliothèque d’images réactive est un module JavaScript qui ajuste dynamiquement la qualité des images diffusées à partir de Dynamic Media et incorporées dans des pages Web réactives. En outre, il offre une meilleure qualité d’image sur les périphériques dotés d’écrans haute densité. La bibliothèque peut également rendre de manière responsable les résultats de la recadrage dynamique et de la série d’échantillons dynamique.
solution: Experience Manager
title: A propos de la bibliothèque d’images réactives
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 0%

---


# A propos de la bibliothèque d’images réactives{#about-responsive-image-library}

La bibliothèque d’images réactive est un module JavaScript qui ajuste dynamiquement la qualité des images diffusées à partir de Dynamic Media et incorporées dans des pages Web réactives. En outre, il offre une meilleure qualité d’image sur les périphériques dotés d’écrans haute densité. La bibliothèque peut également rendre de manière responsable les résultats de la recadrage dynamique et de la série d’échantillons dynamique.

## URL de démonstration {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Le cas d’utilisation le plus simple de la bibliothèque d’images réactive consiste à définir une liste de valeurs de points d’arrêt pour la largeur de l’image. Cette liste permet de s’assurer que le rendu approprié est chargé et affiché lorsqu’une image est redimensionnée en raison de la mise en page de la page Web qui change depuis qu’un utilisateur redimensionne la fenêtre du navigateur ou modifie l’orientation du périphérique. La bibliothèque surveille en permanence la taille des images à l’écran et, chaque fois qu’une nouvelle largeur de point d’arrêt est atteinte, elle récupère un nouveau rendu d’image à partir de Dynamic Media.

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
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>Voici un exemple simple où l’image adaptée se trouve dans un conteneur qui prend 50 % de la largeur de la page Web. Chaque fois que la fenêtre du navigateur est redimensionnée, la largeur du conteneur change. Lorsque la largeur de l’image atteint l’un des points d’arrêt configurés (définis à 200, 400, 600 et 800 pixels à des fins d’illustration), un nouveau rendu est téléchargé et affiché. L’objectif est d’éviter de charger des images volumineuses inutiles et d’économiser la bande passante du réseau. </p> <p>Cliquez sur l’URL pour ouvrir la page Web, redimensionner la fenêtre du navigateur et surveiller le trafic réseau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>L’exemple de Bootstrap suivant illustre le même cas d’utilisation dans une page Web. Selon le CSS Bootstrap, la cellule de disposition à laquelle l’image adaptée est ajoutée peut avoir l’une des largeurs suivantes : 360, 720 et 940 pixels. Il s’agit des valeurs exactes transmises en tant que points d’arrêt à la bibliothèque d’images réactive. Ainsi, Dynamic Media s'assure que la bande passante réseau du client est utilisée efficacement. De plus, il garantit également que l’image est affichée à la taille exacte requise, compte tenu de la mise en page Web actuelle, sans artefacts visuels lors de la mise à l’échelle du navigateur côté client. </p> <p>Cliquez sur l’URL pour ouvrir la page Web, redimensionnez la fenêtre du navigateur pour accéder à différents points d’arrêt de la mise en page et surveillez le trafic réseau. </p> <p>Les cas d’utilisation plus avancés incluent l’association de différents paramètres d’image prédéfinis, ou de commandes de diffusion d’images, ou les deux, à des valeurs de points d’arrêt différentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>Dans l’exemple suivant, des paramètres d’image prédéfinis de qualité et de format différents pour différentes tailles de points d’arrêt sont utilisés. Pour un petit point d’arrêt, un paramètre prédéfini de faible qualité est appliqué, ce qui force Image Serving à renvoyer l’image GIF compressée à six couleurs uniquement. Un point d’arrêt moyen utilise un paramètre d’image prédéfini configuré pour le format JPEG avec une compression élevée. Le point d’arrêt le plus important est associé à un paramètre d’image prédéfini de haute qualité à l’aide d’un fichier PNG sans perte. Cette méthode garantit la diffusion d’images de haute qualité sur ces périphériques, en partant du principe que les périphériques dotés d’écrans plus grands disposent d’une bande passante et d’une puissance de traitement plus importantes. </p> <p>Cliquez sur l’URL pour ouvrir la page Web, redimensionnez la fenêtre du navigateur Web de plus en plus grande et notez la dégradation de la qualité de l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Outre les paramètres d’image prédéfinis, il est possible d’associer des commandes de diffusion d’images spécifiques à des points d’arrêt. L’exemple suivant montre comment il est possible de recadrer progressivement l’image de la bannière dans la zone d’intérêt à mesure que la taille de l’image à l’écran devient plus petite. Ici, le point d’arrêt le plus grand ne comporte aucune commande de diffusion d’images, de sorte que l’image de la bannière est entièrement visible. A un point d’arrêt moyen applique un recadrage modéré, ce qui rend visible uniquement le coureur dont le texte est "En cours". À un petit point d’arrêt, davantage de recadrage est appliqué afin que seul le produit s’affiche. </p> <p>Cliquez sur l’URL pour ouvrir la page Web et redimensionner la fenêtre de votre navigateur. Remarquez comment l'image se recadre progressivement lorsque vous passez d'une taille plus grande à une taille plus petite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>Vous pouvez également utiliser des commandes de diffusion d’images avec des modèles de diffusion d’images pour contrôler certains paramètres de modèle en fonction de la taille de l’image. Dans l’exemple suivant, un modèle de diffusion d’images est utilisé lorsque la taille de police de l’incrustation de texte est paramétrée à l’aide du paramètre <span class="codeph"> $fontsize </span>. L’image réactive est configurée de manière à utiliser une taille de police plus grande pour les images de taille plus petite afin de s’assurer que le texte reste toujours lisible : </p> </td> 
  </tr> 
 </tbody> 
</table>

## Configuration système requise {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Matériel et logiciels du serveur**

* Dynamic Media Image Serving 6.0.1 ou version ultérieure.

**Configuration minimale requise pour le navigateur client**

* Microsoft® Windows® 7 ou version ultérieure ; Mac OS X 10.8 ou version ultérieure.
* Firefox 23, Safari 6, Chrome 29, IE 9 ou version ultérieure.
* iOS 6 ou version ultérieure.
* Certifié sur iPhone3GS ou une version ultérieure et iPad2 ou une version ultérieure (navigateurs natifs uniquement).
* Android OS 2.3 ou version ultérieure.
* Pour le moment, Internet Explorer sur les périphériques mobiles n’est pas pris en charge.

