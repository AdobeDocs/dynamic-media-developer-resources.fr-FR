---
title: Utilisation de la bibliothèque d’images réactive
description: Pour ajouter une bibliothèque d’images réactive à une page web et gérer les images existantes avec la bibliothèque, procédez comme suit.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Utilisation de la bibliothèque d’images réactive{#using-responsive-image-library}

Pour ajouter une bibliothèque d’images réactive à une page web et gérer les images existantes avec la bibliothèque, procédez comme suit.

**Pour utiliser la bibliothèque d’images réactive**

1. Dans Dynamic Media Classic, [créez un paramètre d’image prédéfini](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) au cas où vous envisageriez d’utiliser la bibliothèque d’images réactive avec des paramètres prédéfinis.

   Lorsque vous définissez des paramètres d’image prédéfinis utilisés avec la bibliothèque d’images réactive, n’utilisez aucun paramètre affectant la taille de l’image, tel que `wid=`, `hei=` ou `scl=`. Ne spécifiez aucun champ de taille dans le paramètre d’image prédéfini. Au lieu de cela, laissez-les comme valeurs vides.
1. Ajoutez le fichier JavaScript de bibliothèque à votre page web.

   Avant de pouvoir utiliser l’API de bibliothèque, veillez à inclure `responsive_image.js`. Ce fichier JavaScript se trouve dans le sous-dossier `libs/` de votre déploiement d’observateurs IS standard :

   `<s7viewers_root>/libs/responsive_image.js`
1. Configurez les images existantes.

   La bibliothèque lit certains attributs de configuration à partir d’une instance d’image avec laquelle elle travaille. Définissez des attributs avant l’appel de la fonction API `s7responsiveImage` pour une telle image.

   Il est également suggéré de placer l’URL de l’image existante dans l’attribut `data-src`. Ensuite, configurez l’attribut `src` existant pour qu’une image GIF 1x1 soit codée en tant qu’URI de données. Cela permet de réduire le nombre de requêtes HTTP envoyées par la page web au moment du chargement. Notez toutefois que si l’optimisation du moteur de recherche (SEO) est nécessaire, il est préférable de configurer un attribut `title` sur l’instance d’image.

<!--
   The following is an example of defining `data-breakpoints` attribute for the image and using a 1x1 GIF encoded as Data URI:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```
-->

1. Appelez la fonction API `s7responsiveImage` pour chaque instance d’image gérée par la bibliothèque.

   Appelez la fonction API `s7responsiveImage` pour chaque instance d’image gérée par la bibliothèque. Après un tel appel, la bibliothèque remplace l’image d’origine par l’image téléchargée à partir de la Diffusion d’images en fonction de la taille d’exécution de l’élément `IMG` dans la disposition de la page web et de la densité de l’écran de l’appareil.

   Le code suivant est un exemple d’appel de `s7responsiveImage` fonction API sur une image, en supposant que `responsiveImage` soit un identifiant de cette image :

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Exemple {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

La bibliothèque prend en charge l’utilisation simultanée de plusieurs instances d’image sur la page web. Par conséquent, répétez les étapes 1 et 2 ci-dessus pour chaque image que vous souhaitez que la bibliothèque gère.

Il est de la responsabilité de la page web de mettre en forme l’élément d’image afin de le rendre flexible en termes de taille. La bibliothèque d’images réactive ne fait pas de distinction entre les images de taille fixe et les images « fluides ». Si elle est appliquée à une image de taille fixe, elle charge la nouvelle image une seule fois.

<!--
The following code is a complete example of a trivial web page that has a single fluid image managed by the Responsive Image library. The example contains extra CSS styling to make the image "responsive" to the web browser window size:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>

```
-->

**Utilisation du recadrage intelligent**

Deux modes de recadrage intelligent sont disponibles dans AEM 6.4 et dans les visionneuses Dynamic Media 5.9 :

* **Manuel** - les points d’arrêt définis par l’utilisateur et les commandes du service d’image correspondantes sont définis dans un attribut de l’élément image.
* **Recadrage intelligent** : les rendus de recadrage intelligent calculés sont automatiquement récupérés à partir du serveur de diffusion. Le meilleur rendu est sélectionné à l’aide de la taille d’exécution de l’élément d’image.

Pour utiliser le mode Recadrage intelligent , définissez l’attribut `data-mode` sur `smart crop`. Par exemple :

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

L’élément image associé distribue un événement `s7responsiveViewer` lors de l’exécution lorsque le point d’arrêt change.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
