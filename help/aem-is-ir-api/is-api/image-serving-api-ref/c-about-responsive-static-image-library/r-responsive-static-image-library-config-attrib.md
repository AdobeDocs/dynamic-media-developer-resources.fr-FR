---
description: Les attributs de configuration sont définis comme des attributs directement sur un élément IMG géré par la bibliothèque d’images réactives. Chaque image peut avoir son propre jeu d’attributs.
seo-description: Les attributs de configuration sont définis comme des attributs directement sur un élément IMG géré par la bibliothèque d’images réactives. Chaque image peut avoir son propre jeu d’attributs.
seo-title: Référence de commande - Attributs de configuration
solution: Experience Manager
title: Référence de commande - Attributs de configuration
topic: Scene7 Image Serving - Image Rendering API
uuid: a3d52680-2a28-40c8-9b5f-b1c252c88e4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Les attributs de configuration sont définis comme des attributs directement sur un élément IMG géré par la bibliothèque d’images réactives. Chaque image peut avoir son propre jeu d’attributs.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Facultatif.

URL de l’image diffusée par la diffusion d’images. Si l’URL n’est pas présente, la bibliothèque utilise la valeur définie dans `src` l’attribut comme valeur de retour en arrière. Cet attribut sert l’image initiale et l’image dynamique que la bibliothèque d’images réactives gère à différents emplacements.

**Exemple**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Si `data-src` est défini, `src` est facultatif et peut contenir toute URL à ajouter. Par exemple, il peut contenir une URL vers la même image basée sur hébergeur d’images que celle utilisée par la bibliothèque. Il peut également contenir un espace réservé GIF, ou même un URI de données, pour éviter un tour de serveur supplémentaire au démarrage.

Si elle `data-src` n’est pas définie, `src` est obligatoire et doit contenir une URL vers l’image diffusée par la diffusion d’images.

**Exemple**

Utilisation de l’URI de données pour l’ `src` attribut et de l’URL de diffusion d’images pour l’ `data-src` attribut :

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## points d’arrêt de données {#section-3bf62a89ff3e40569848c1fe3ac7886c}

de points d’arrêt séparés par des virgules, suivi éventuellement de deux points ( `:`), de commandes de diffusion d’images ou de paramètres d’image prédéfinis. Chaque point d’arrêt est une valeur de largeur d’image définie en pixels CSS logiques. La bibliothèque charge l’image avec la valeur la plus élevée du et la réduit sur le client pour qu’elle corresponde à la largeur de l’image CSS au moment de l’exécution. (Si vous travaillez sur un écran haute densité, les rendus d’image chargés à partir du serveur représentent des valeurs de point d’arrêt multipliées par le rapport des pixels du périphérique).

Pour tout point d’arrêt du, il est possible de définir une ou plusieurs commandes de diffusion d’images ou des noms de paramètres d’image prédéfinis. Ces paramètres supplémentaires ne sont appliqués à l’image que si ce point d’arrêt particulier est actif.

Vous pouvez utiliser n’importe quelle commande de diffusion d’images prise en charge, à l’exception des commandes  qui affectent la taille de l’image de réponse, comme `wid=`, `hei=`ou `scl=`. La même restriction s’applique aux paramètres d’image prédéfinis : un paramètre d’image prédéfini utilisé avec la bibliothèque d’images réactive ne doit pas contenir de telles commandes.

Plusieurs commandes de diffusion d’images ou noms de paramètres d’image prédéfinis sont séparés par le caractère &quot; `&`&quot;. Si la valeur d’une commande de diffusion d’images est une virgule, cette dernière est remplacée par `%2C`. Les noms des paramètres d’image prédéfinis sont encapsulés dans des signes dollar ( `$`).

**Exemples**

**Utilisation des points d’arrêt uniquement**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Utilisation des commandes de diffusion d’images**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Utilisation des paramètres d’image prédéfinis**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Utilisation des paramètres d’image prédéfinis et des commandes de diffusion d’images**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Les deux modes de recadrage dynamique suivants sont disponibles dans AEM 6.4 et versions ultérieures et dans Scene7 Viewers 5.9 et versions ultérieures :

* **Manuel** : les points d’arrêt définis par l’utilisateur et les commandes correspondantes du service d’images sont définis dans un attribut de l’élément d’image.
* **Recadrage** dynamique : les rendus de recadrage dynamique calculés sont automatiquement récupérés à partir du serveur . Le meilleur rendu est sélectionné à l’aide de la taille d’exécution de l’élément d’image.

Pour utiliser le mode Recadrage dynamique, définissez l’ `data-mode` attribut sur `smart crop`.

**Exemple**

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

