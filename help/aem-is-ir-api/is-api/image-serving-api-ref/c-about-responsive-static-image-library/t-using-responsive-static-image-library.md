---
title: Utilisation de la bibliothèque d’images réactives
description: Pour ajouter une bibliothèque d’images réactives à une page web et gérer les images existantes avec la bibliothèque, procédez comme suit.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Utilisation de la bibliothèque d’images réactives{#using-responsive-image-library}

Pour ajouter une bibliothèque d’images réactives à une page web et gérer les images existantes avec la bibliothèque, procédez comme suit.

**Pour utiliser la bibliothèque d’images réactives**

1. Dans Dynamic Media Classic, [créez un paramètre d’image prédéfini](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) si vous envisagez d’utiliser la bibliothèque d’images réactives avec des paramètres prédéfinis.

   Lorsque vous définissez des paramètres d’image prédéfinis utilisés avec la bibliothèque d’images réactives, n’utilisez aucun paramètre qui affecte la taille de l’image, comme `wid=`, `hei=` ou `scl=`. Ne spécifiez aucun champ de taille dans le paramètre d’image prédéfini. Conservez plutôt des valeurs vides.
1. Ajoutez le fichier JavaScript de bibliothèque à votre page web.

   Avant de pouvoir utiliser l’API de bibliothèque, veillez à inclure `responsive_image.js`. Ce fichier JavaScript se trouve dans le sous-dossier `libs/` de votre déploiement IS-Viewers standard :

   `<s7viewers_root>/libs/responsive_image.js`
1. Configurez les images existantes.

   La bibliothèque lit certains attributs de configuration à partir d’une instance d’image avec laquelle elle travaille. Définissez des attributs avant l’appel de la fonction d’API `s7responsiveImage` pour une telle image.

   Il est également conseillé de placer l’URL de l’image existante dans l’attribut `data-src` . Ensuite, configurez l’attribut `src` existant pour qu’une image de GIF 1x1 soit codée en tant qu’URI de données. Cela permet de réduire le nombre de requêtes HTTP envoyées par la page web au moment du chargement. Notez toutefois que si le SEO (optimisation du moteur de recherche) est nécessaire, il est préférable de configurer un attribut `title` sur l’instance d’image.

   Voici un exemple de définition de l’attribut `data-breakpoints` pour l’image à l’aide d’un GIF 1x1 encodé en tant qu’URI de données :

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Appelez la fonction d’API `s7responsiveImage` pour chaque instance d’image gérée par la bibliothèque.

   Appelez la fonction d’API `s7responsiveImage` pour chaque instance d’image gérée par la bibliothèque. Après un tel appel, la bibliothèque remplace l’image d’origine par l’image téléchargée à partir du serveur d’images en fonction de la taille d’exécution de l’élément `IMG` dans la mise en page web et de la densité de l’écran de l’appareil.

   Le code suivant est un exemple d’appel de la fonction d’API `s7responsiveImage` sur une image, en supposant que `responsiveImage` soit un identifiant de cette image :

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Exemple {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

La bibliothèque prend en charge l’utilisation simultanée de nombreuses instances d’image sur la page web. Par conséquent, répétez les étapes 1 et 2 ci-dessus pour chaque image que vous souhaitez que la bibliothèque gère.

Il est de la responsabilité de la page web de mettre en forme l’élément image afin de le rendre flexible en termes de taille. La bibliothèque d’images réactives ne fait pas de distinction entre les images de taille fixe et les images &quot;fluides&quot;. S’il est appliqué à une image à taille fixe, il ne charge la nouvelle image qu’une seule fois.

Le code suivant est un exemple complet d’une page web triviale qui comporte une seule image fluide gérée par la bibliothèque d’images réactives. L’exemple contient un style CSS supplémentaire pour rendre l’image &quot;réactive&quot; à la taille de la fenêtre du navigateur web :

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

**Utilisation du recadrage intelligent**

Deux modes de recadrage intelligent sont disponibles dans AEM 6.4 et dans Dynamic Media Viewers 5.9 :

* **Manuel** - Les points d’arrêt définis par l’utilisateur et les commandes correspondantes du service d’image sont définis dans un attribut de l’élément image.
* **Recadrage intelligent** : les rendus de recadrage intelligent calculé sont automatiquement récupérés à partir du serveur de diffusion. Le meilleur rendu est sélectionné à l’aide de la taille d’exécution de l’élément d’image.

Pour utiliser le mode Recadrage intelligent, définissez l’attribut `data-mode` sur `smart crop`. Par exemple :

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

L’élément d’image associé distribue un événement `s7responsiveViewer` au moment de l’exécution lorsque le point d’arrêt change.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
