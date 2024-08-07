---
description: Le service d’images met en oeuvre une fonction de filigrane visuelle simple.
solution: Experience Manager
title: Filigranes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Filigranes{#watermarks}

Le service d’images met en oeuvre une fonction de filigrane visuelle simple.

Un filigrane est généralement une image semi-transparente, mais il peut s’agir de texte ou d’une image composite à couches plus complexes. Le serveur couche le filigrane sur l’image de réponse après l’application de tous les attributs d’affichage ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`).

Le filigrane est activé en définissant `attribute::Watermark` sur une entrée de catalogue valide contenant l’image ou le modèle de filigrane. Si `attribute::Watermark` est défini dans un catalogue nommé, le serveur ajoute le filigrane à toutes les demandes d’image qui référencent l’ID de catalogue dans l’URL de la demande. Si `default::Watermark` est défini (dans le catalogue par défaut, [!DNL default.ini]), le filigrane est appliqué à toutes les demandes d’image, qu’elles fassent référence à un catalogue ou non.

Les filigranes ne sont pas appliqués aux images renvoyées en réponse aux demandes de miniatures ( `req=tmb`) et à certaines demandes des visionneuses Dynamic Media.

## Mise à l&#39;échelle et alignement {#section-89ef9e5926ae438abbd8e70332749b76}

Lorsqu’un filigrane est spécifié, le serveur génère d’abord l’image composite (l’ *image cible*) à laquelle le filigrane doit être appliqué (avant d’appliquer les transformations de vue). Le serveur génère ensuite l’image composite pour le filigrane comme toute autre image (l’ *image de filigrane*).

Contrairement aux images standard, `sizeN=` peut être spécifié pour layer=0 ou layer=comp de l’image de filigrane. Cela permet de mettre à l’échelle l’image du filigrane par rapport à l’image cible. Si `sizeN=` n’est pas spécifié, l’image du filigrane conserve sa taille en pixels lors de la fusion avec l’image cible.

Les commandes de requête (telles que `fmt=`) et les commandes d’affichage (telles que `wid=`) sont ignorées dans les enregistrements de filigrane, à l’exception de `align=`. `align=` peut être utilisé pour positionner l’image du filigrane par rapport à l’image du filigrane par rapport à l’image cible. Cela permet de positionner le filigrane par rapport à un coin ou à un bord de l’image cible.

Après la mise à l’échelle et l’alignement, le serveur calque l’image du filigrane sur l’image cible à l’aide des valeurs `blendMode=` et `opac=` spécifiées pour `layer=0` ou `layer=comp` de l’image du filigrane. Enfin, les commandes de requête et d’affichage spécifiées pour l’image cible sont appliquées pour construire l’image de réponse.

Notez que l’image du filigrane ne s’étend jamais sur un espace vide ajouté à l’image de réponse par les commandes `wid=` et `hei=`.

## Exemple {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Un filigrane type peut être constitué d’une simple image RGBA contenant un logo ou un avis de copyright. Nous créons un enregistrement dans le catalogue d’images (ou le catalogue par défaut) avec `catalog::Id` défini sur `watermark` et spécifions le fichier image de filigrane dans `catalog::Path`. Nous voulons étirer le filigrane pour l’adapter à l’image d’affichage (sans déformer le filigrane) tout en laissant une marge supplémentaire, et réduire l’opacité à 20 % du filigrane d’origine, nous avons donc défini `catalog::Modifier` sur `sizeN=0.9,0.9&opac=20`. Pour activer le filigrane, définissez `attribute::Watermark` sur l’identifiant de l’entrée du catalogue de filigranes, &quot;filigrane&quot; dans cet exemple. Nous pouvons essayer différents `blendMode=` choix pour obtenir différents effets de filigrane.

## Voir aussi {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
