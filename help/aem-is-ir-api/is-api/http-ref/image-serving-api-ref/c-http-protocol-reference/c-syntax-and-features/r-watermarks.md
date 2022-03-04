---
description: Le service d’images met en oeuvre une fonction de filigrane visuelle simple.
solution: Experience Manager
title: Filigranes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 1%

---

# Filigranes{#watermarks}

Le service d’images met en oeuvre une fonction de filigrane visuelle simple.

Un filigrane est généralement une image semi-transparente, mais il peut s’agir de texte ou d’une image composite à couches plus complexes. Le serveur calque le filigrane sur l’image de réponse après tous les attributs d’affichage ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) ont été appliquées.

Le filigrane est activé en définissant `attribute::Watermark` à une entrée de catalogue valide contenant l’image ou le modèle de filigrane. If `attribute::Watermark` est défini dans un catalogue nommé, le serveur ajoute le filigrane à toutes les demandes d’image qui référencent l’ID de catalogue dans l’URL de la demande. If `default::Watermark` est défini (dans le catalogue par défaut, [!DNL default.ini]), le filigrane est appliqué à toutes les demandes d’image, qu’elles fassent référence à un catalogue ou non.

Les filigranes ne sont pas appliqués aux images renvoyées en réponse aux demandes de miniatures ( `req=tmb`) et certaines requêtes provenant des visionneuses Dynamic Media.

## Mise à l&#39;échelle et alignement {#section-89ef9e5926ae438abbd8e70332749b76}

Lorsqu’un filigrane est spécifié, le serveur génère d’abord l’image composite (la variable *image cible*) auquel le filigrane doit être appliqué (avant d’appliquer les transformations de vue). Le serveur génère ensuite l’image composite pour le filigrane, comme toute autre image (le *image de filigrane*).

Contrairement aux images standard, `sizeN=` peut être spécifié pour layer=0 ou layer=comp de l’image de filigrane. Cela permet de mettre à l’échelle l’image du filigrane par rapport à l’image cible. If `sizeN=` n’est pas spécifié, l’image de filigrane conserve sa taille en pixels lors de la fusion avec l’image cible.

Commandes de requête (telles que `fmt=`) et les commandes d’affichage (telles que `wid=`) sont ignorées dans les enregistrements de filigrane, à l’exception de `align=`. `align=` peut être utilisé pour positionner l’image du filigrane par rapport à l’image cible. Cela permet de positionner le filigrane par rapport à un coin ou à un bord de l’image cible.

Après la mise à l’échelle et l’alignement, le serveur superpose l’image du filigrane sur l’image cible à l’aide de la fonction `blendMode=` et `opac=` valeurs spécifiées pour `layer=0` ou `layer=comp` de l’image de filigrane. Enfin, les commandes de requête et d’affichage spécifiées pour l’image cible sont appliquées pour construire l’image de réponse.

Notez que l’image de filigrane ne s’étend jamais sur un espace vide ajouté à l’image de réponse par la fonction `wid=` et `hei=` des commandes.

## Exemple {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Un filigrane type peut être constitué d’une simple image RGBA contenant un logo ou un avis de copyright. Nous créons un enregistrement dans le catalogue d’images (ou le catalogue par défaut) avec `catalog::Id` défini sur `watermark` et spécifiez le fichier image de filigrane dans `catalog::Path`. Nous voulons étirer le filigrane pour l’adapter à l’image (sans déformer le filigrane) tout en laissant une marge supplémentaire, et réduire l’opacité à 20 % du filigrane d’origine, nous définissons donc `catalog::Modifier` to `sizeN=0.9,0.9&opac=20`. Pour activer le filigrane, définissez `attribute::Watermark` à l’identifiant de l’entrée du catalogue de filigranes, &quot;filigrane&quot; dans cet exemple. Nous pourrions vouloir expérimenter avec différentes `blendMode=` choix permettant d’obtenir différents effets de filigrane.

## Voir aussi {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
