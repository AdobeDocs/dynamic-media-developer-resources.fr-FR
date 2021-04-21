---
description: Pour ajouter une bibliothèque d’images réactives à une page Web et gérer les images existantes avec la bibliothèque, procédez comme suit.
solution: Experience Manager
title: Utilisation de la bibliothèque d’images réactives
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 0%

---


# Utilisation de la bibliothèque d’images réactives{#using-responsive-image-library}

Pour ajouter une bibliothèque d’images réactives à une page Web et gérer les images existantes avec la bibliothèque, procédez comme suit.

**Pour utiliser la bibliothèque d’images réactives**

1. Dans Dynamic Media Classic, [créez un paramètre d’image prédéfini](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) au cas où vous envisageriez d’utiliser la bibliothèque d’images réactives avec des paramètres prédéfinis.

   Lorsque vous définissez des paramètres d’image prédéfinis utilisés avec la bibliothèque d’images réactive, n’utilisez aucun paramètre qui affecte la taille de l’image, tel que `wid=`, `hei=` ou `scl=`. Ne spécifiez aucun champ de taille dans le paramètre d’image prédéfini. Laissez-les en lieu et place comme des valeurs vides.
1. Ajoutez le fichier JavaScript de bibliothèque sur votre page Web.

   Avant de pouvoir utiliser l&#39;API de bibliothèque, veillez à inclure `responsive_image.js`. Ce fichier JavaScript se trouve dans le sous-dossier `libs/` de votre déploiement des visionneuses IS standard :

   `<s7viewers_root>/libs/responsive_image.js`
1. Configurez les images existantes.

   La bibliothèque lit certains attributs de configuration à partir d’une instance d’image sur laquelle elle travaille. Définissez des attributs avant l&#39;appel de la fonction API `s7responsiveImage` pour une telle image.

   Il est également conseillé de placer l’URL d’image existante dans l’attribut `data-src`. Ensuite, configurez l’attribut `src` existant pour qu’une image GIF 1x1 soit codée en tant qu’URI de données. Cela permet de réduire le nombre de requêtes HTTP envoyées par la page Web au moment du chargement. Notez toutefois que si le référencement (optimisation du moteur de recherche) est nécessaire, il est préférable de configurer un attribut `title` sur l’instance d’image.

   Voici un exemple de définition de l’attribut `data-breakpoints` pour l’image et d’utilisation d’un GIF 1x1 codé en tant qu’URI de données :

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Appelez la fonction d&#39;API `s7responsiveImage` pour chaque instance d&#39;image gérée par la bibliothèque.

   Appelez la fonction d&#39;API `s7responsiveImage` pour chaque instance d&#39;image gérée par la bibliothèque. Après un tel appel, la bibliothèque remplace l’image d’origine par l’image téléchargée à partir de la diffusion d’images en fonction de la taille d’exécution de l’élément `IMG` dans la mise en page de la page Web et de la densité de l’écran du périphérique.

   Le code suivant est un exemple d&#39;appel de la fonction d&#39;API `s7responsiveImage` sur une image, en supposant que `responsiveImage` soit un identifiant de cette image :

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Exemple {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

La bibliothèque prend en charge l’utilisation simultanée de nombreuses instances d’image sur la page Web. Par conséquent, répétez les étapes 1 et 2 ci-dessus pour chaque image à gérer par la bibliothèque.

Il est de la responsabilité de la page Web de mettre en forme l’élément d’image pour le rendre flexible en termes de taille. La bibliothèque d’images réactives elle-même ne fait pas de distinction entre les images de taille fixe et les images &quot;fluides&quot;. Si elle est appliquée à une image de taille fixe, elle ne charge la nouvelle image qu’une seule fois.

Le code suivant est un exemple complet d’une page Web triviale dont une seule image fluide est gérée par la bibliothèque d’images réactives. L’exemple contient un style CSS supplémentaire pour rendre l’image &quot;adaptée&quot; à la taille de la fenêtre du navigateur Web :

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

**Utilisation de la recadrage intelligente**

Il existe deux modes de recadrage dynamique disponibles dans AEM 6.4 et Dynamic Media Viewers 5.9 :

* **Les points d’arrêt définis manuellement**  par l’utilisateur et les commandes correspondantes du service d’images sont définis dans un attribut de l’élément d’image.
* **Recadrage**  dynamique : les rendus de recadrage intelligent calculés sont automatiquement récupérés à partir du serveur de diffusion. Le meilleur rendu est sélectionné en utilisant la taille d’exécution de l’élément d’image.

Pour utiliser le mode Recadrage dynamique, définissez l&#39;attribut `data-mode` sur `smart crop`. Par exemple :

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

L’élément d’image associé distribue un événement `s7responsiveViewer` pendant l’exécution lorsque le point d’arrêt change.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
