---
description: Pour ajouter une bibliothèque d’images réactives à une page Web et gérer les images existantes avec la bibliothèque, procédez comme suit.
seo-description: Pour ajouter une bibliothèque d’images réactives à une page Web et gérer les images existantes avec la bibliothèque, procédez comme suit.
seo-title: Utilisation de la bibliothèque d’images réactives
solution: Experience Manager
title: Utilisation de la bibliothèque d’images réactives
topic: Scene7 Image Serving - Image Rendering API
uuid: 325cdc8d-2bfa-4f9b-bf88-51d1dcc6c495
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# Utilisation de la bibliothèque d’images réactives{#using-responsive-image-library}

Pour ajouter une bibliothèque d’images réactives à une page Web et gérer les images existantes avec la bibliothèque, procédez comme suit.

**Pour utiliser la bibliothèque d’images réactives**

1. Dans SPS, [créez un paramètre](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html) d’image prédéfini au cas où vous envisageriez d’utiliser la bibliothèque d’images réactives avec des paramètres prédéfinis.

   Lorsque vous définissez des paramètres d’image prédéfinis qui sont utilisés avec la bibliothèque d’images réactive, n’utilisez aucun paramètre qui affecte la taille de l’image, tel que `wid=`, `hei=`ou `scl=`. Ne spécifiez aucun champ de taille dans le paramètre d’image prédéfini. Laissez-les comme des valeurs vides.
1. Ajouter le fichier JavaScript de bibliothèque dans votre page Web.

   Avant d’utiliser l’API de bibliothèque, veillez à inclure `responsive_image.js`. Ce fichier JavaScript se trouve dans le `libs/` sous-dossier du déploiement des visionneuses IS standard :

   `<s7viewers_root>/libs/responsive_image.js`
1. Configurez les images existantes.

   La bibliothèque lit certains attributs de configuration d’une instance d’image sur laquelle elle travaille. Définissez des attributs avant que la fonction `s7responsiveImage` API ne soit appelée pour une telle image.

   Il est également conseillé de placer l’URL d’image existante dans l’ `data-src` attribut. Configurez ensuite l’ `src` attribut existant pour qu’une image GIF 1x1 soit codée en tant qu’URI de données. Cela permet de réduire le nombre de requêtes HTTP envoyées par la page Web au moment du chargement. Notez toutefois que si le référencement (optimisation du moteur de recherche) est nécessaire, il est préférable de configurer un `title` attribut sur l’instance d’image.

   Voici un exemple de définition d’ `data-breakpoints` attribut pour l’image et d’utilisation d’un fichier GIF 1x1 codé en tant qu’URI de données :

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Appelez la fonction `s7responsiveImage` API pour chaque instance d’image gérée par la bibliothèque.

   Appelez la fonction `s7responsiveImage` API pour chaque instance d’image gérée par la bibliothèque. Après un tel appel, la bibliothèque remplace l’image d’origine par l’image téléchargée à partir de la diffusion d’images en fonction de la taille d’exécution de l’ `IMG` élément dans la mise en page Web et de la densité de l’écran du périphérique.

   Le code suivant est un exemple d’appel de la fonction `s7responsiveImage` API sur une image, en supposant qu’ `responsiveImage` il s’agisse d’un identifiant de cette image :

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Exemple {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

La bibliothèque prend en charge l’utilisation simultanée de nombreuses instances d’image sur la page Web. Par conséquent, répétez les étapes 1 et 2 ci-dessus pour chaque image que vous souhaitez que la bibliothèque gère.

Il est de la responsabilité de la page Web de mettre en forme l’élément d’image pour le rendre flexible en termes de taille. La bibliothèque d’images réactives elle-même ne fait pas de distinction entre les images de taille fixe et les images &quot;fluides&quot;. S’il est appliqué à une image de taille fixe, il ne charge la nouvelle image qu’une seule fois.

Le code suivant est un exemple complet d’une page Web triviale avec une image fluide unique gérée par la bibliothèque d’images réactives. L’exemple contient un style CSS supplémentaire pour rendre l’image &quot;adaptée&quot; à la taille de la fenêtre du navigateur Web :

```
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

**Utilisation du recadrage intelligent**

Deux modes de recadrage dynamique sont disponibles dans AEM 6.4 et dans les visionneuses Scene7 5.9 :

* **Manuel** : les points d’arrêt définis par l’utilisateur et les commandes correspondantes du service d’images sont définis dans un attribut de l’élément d’image.
* **Recadrage** dynamique : les rendus de recadrage dynamique calculés sont automatiquement récupérés à partir du serveur . Le meilleur rendu est sélectionné à l’aide de la taille d’exécution de l’élément d’image.

Pour utiliser le mode Recadrage dynamique, définissez l’ `data-mode` attribut sur `smart crop`. Par exemple :

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

L’élément d’image associé distribue un `s7responsiveViewer` au cours de l’exécution lorsque le point d’arrêt change.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
