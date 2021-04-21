---
description: Image Serving implémente un filigrane visuel simple.
solution: Experience Manager
title: Filigranes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 1%

---


# Filigranes{#watermarks}

Image Serving implémente un filigrane visuel simple.

Un filigrane est généralement une image semi-transparente, mais il peut s’agir de texte ou d’une image composite superposée plus complexe. Le serveur superpose le filigrane sur l’image de réponse après l’application de tous les attributs de vue ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`).

Le filigrane est activé en définissant `attribute::Watermark` sur une entrée de catalogue valide qui contiendra l&#39;image ou le modèle de filigrane. Si `attribute::Watermark` est défini dans un catalogue nommé, le serveur ajoute le filigrane à toutes les demandes d’image qui référencent l’ID de catalogue dans l’URL de demande. Si `default::Watermark` est défini (dans le catalogue par défaut, [!DNL default.ini]), le filigrane sera appliqué à toutes les demandes d&#39;image, qu&#39;elles référencent un catalogue ou non.

Les filigranes ne sont pas appliqués aux images renvoyées en réponse à des requêtes de miniatures ( `req=tmb`) et à certaines requêtes des visionneuses Dynamic Media.

## Mise à l’échelle et alignement {#section-89ef9e5926ae438abbd8e70332749b76}

Lorsqu’un filigrane est spécifié, le serveur génère d’abord l’image composite (l’*image de cible*) à laquelle le filigrane doit être appliqué (avant d’appliquer les transformations de vue). Le serveur génère ensuite l’image composite pour le filigrane comme toute autre image (l’*image de filigrane*).

Contrairement aux images standard, `sizeN=` peut être spécifié pour layer=0 ou layer=comp de l’image de filigrane. Cela permet de mettre à l’échelle l’image du filigrane par rapport à l’image de la cible. Si `sizeN=` n’est pas spécifié, l’image de filigrane conserve sa taille en pixels lors de la fusion avec l’image de cible.

Les commandes de requête (telles que `fmt=`) et les commandes de vue (telles que `wid=`) sont ignorées dans les enregistrements de filigrane, à l&#39;exception de `align=`. `align=` peut être utilisé pour positionner l’image du filigrane par rapport à l’image du filigrane par rapport à l’image de la cible. Cela permet de positionner le filigrane par rapport à un angle ou à un bord de l’image de cible.

Après mise à l’échelle et alignement, le serveur superpose l’image du filigrane sur l’image de la cible en utilisant les valeurs `blendMode=` et `opac=` spécifiées pour `layer=0` ou `layer=comp` de l’image du filigrane. Enfin, les commandes de requête et de vue spécifiées pour l’image de cible sont appliquées pour construire l’image de réponse.

Notez que l’image du filigrane ne s’étend jamais sur un espace vide ajouté à l’image de réponse par les commandes `wid=` et `hei=`.

## Exemple {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Un filigrane type peut être constitué d’une simple image RGBA contenant un logo ou un avis de copyright. Nous créons un enregistrement dans le catalogue d’images (ou le catalogue par défaut) avec `catalog::Id` défini sur `watermark` et nous spécifions le fichier image de filigrane dans `catalog::Path`. Nous voulons étirer le filigrane pour l&#39;adapter à l&#39;image de la vue (sans déformer le filigrane) tout en laissant une marge supplémentaire, et réduire l&#39;opacité à 20% du filigrane d&#39;origine, nous avons donc défini `catalog::Modifier` sur `sizeN=0.9,0.9&opac=20`. Pour activer le filigrane, définissez `attribute::Watermark` sur l&#39;id de l&#39;entrée de catalogue de filigranes, &quot;filigrane&quot; dans cet exemple. Nous pouvons essayer différentes options `blendMode=` pour obtenir différents effets de filigrane.

## Voir aussi {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribut : filigrane](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
