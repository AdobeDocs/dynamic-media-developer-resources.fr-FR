---
description: Les attributs de configuration sont définis comme des attributs directement sur un élément IMG géré par la bibliothèque d’images réactives. Chaque image peut avoir son propre jeu d’attributs.
solution: Experience Manager
title: Référence de commande - Attributs de configuration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Les attributs de configuration sont définis comme des attributs directement sur un élément IMG géré par la bibliothèque d’images réactives. Chaque image peut avoir son propre jeu d’attributs.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Facultatif.

URL de l’image fournie par le serveur d’images. Si l’URL n’est pas présente, la bibliothèque utilise la valeur qui est définie dans l’attribut `src` comme &quot;fall back&quot;. Cet attribut sert l’image initiale et l’image dynamique que la bibliothèque d’images réactives gère à partir de différents emplacements.

**Exemple**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Si `data-src` est défini, `src` est facultatif et peut contenir n’importe quelle URL à ajouter. Par exemple, il peut contenir une URL vers la même image basée sur la diffusion d’images que celle utilisée par la bibliothèque. Il peut également contenir un espace réservé de GIF, ou même un URI de données, afin d’éviter un tour de serveur supplémentaire au démarrage.

Si `data-src` n’est pas défini, `src` est obligatoire et doit contenir une URL vers l’image fournie par le serveur d’images.

**Exemple**

Utilisation de l’URI de données pour l’attribut `src` et de l’URL de diffusion d’images pour l’attribut `data-src` :

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Liste de points d’arrêt séparés par des virgules et éventuellement suivis par deux points ( `:`), commandes de diffusion d’images ou paramètres d’image prédéfinis. Chaque point d’arrêt est une valeur de largeur d’image définie en pixels CSS logiques. La bibliothèque charge l’image avec la valeur la plus élevée la plus proche de la liste et la réduit sur le client pour qu’elle corresponde à la largeur de l’image CSS d’exécution. (Si vous travaillez sur un écran de haute densité, les rendus d’image chargés à partir du serveur représentent les valeurs de point d’arrêt multipliées par le rapport de pixels de l’appareil.)

Pour tout point d’arrêt de la liste, il est possible de définir une ou plusieurs commandes de diffusion d’images ou noms de paramètres d’image prédéfinis. Ces paramètres supplémentaires ne sont appliqués à l’image que si ce point d’arrêt particulier est actuellement actif.

Vous pouvez utiliser n’importe quelle commande de diffusion d’images prise en charge, à l’exception des commandes d’affichage qui affectent la taille de l’image de réponse, comme `wid=`, `hei=` ou `scl=`. La même restriction s’applique aux paramètres d’image prédéfinis : un paramètre d’image prédéfini utilisé avec la bibliothèque d’images réactives ne doit pas contenir de telles commandes.

Plusieurs commandes de diffusion d’images ou noms de paramètres d’image prédéfinis sont séparés par le caractère &quot;`&`&quot;. Si la valeur d’une commande de diffusion d’images contient une virgule, cette virgule est remplacée par `%2C`. Les noms des paramètres d’image prédéfinis sont entourés de signes dollar ( `$`).

**Exemples**

**Utilisation des points d’arrêt uniquement**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Utilisation de commandes de diffusion d’images**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Utilisation de paramètres d’image prédéfinis**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Utilisation des paramètres d’image prédéfinis et des commandes de diffusion d’images**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Les deux modes de recadrage intelligent suivants sont disponibles dans AEM version 6.4 et ultérieure et dans Dynamic Media Viewers 5.9 et versions ultérieures :

* **Manuel** - Les points d’arrêt définis par l’utilisateur et les commandes correspondantes du service d’image sont définis dans un attribut de l’élément image.
* **Recadrage intelligent** : les rendus de recadrage intelligent calculé sont automatiquement récupérés à partir du serveur de diffusion. Le meilleur rendu est sélectionné à l’aide de la taille d’exécution de l’élément d’image.

Pour utiliser le mode Recadrage intelligent, définissez l’attribut `data-mode` sur `smart crop`.

**Exemple**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

L’élément d’image associé distribue un événement `s7responsiveViewer` au moment de l’exécution lorsque le point d’arrêt change.

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
