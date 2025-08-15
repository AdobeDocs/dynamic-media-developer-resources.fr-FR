---
description: Le service d’images met en œuvre une fonctionnalité de filigrane visuel simple.
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

Le service d’images met en œuvre une fonctionnalité de filigrane visuel simple.

Un filigrane est généralement une image semi-transparente, mais il peut s’agir de texte ou d’une image composite superposée plus complexe. Le serveur place le filigrane sur l’image de réponse une fois que tous les attributs d’affichage ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) ont été appliqués.

L’application d’un filigrane est activée en définissant `attribute::Watermark` sur une entrée de catalogue valide qui contiendra l’image ou le modèle du filigrane. Si `attribute::Watermark` est défini dans un catalogue nommé, le serveur ajoute le filigrane à toutes les requêtes d’images qui font référence à l’ID de catalogue dans l’URL de requête. Si `default::Watermark` est défini (dans le catalogue par défaut, [!DNL default.ini]), le filigrane est appliqué à toutes les demandes d’images, qu’elles référencent un catalogue ou non.

Les filigranes ne sont pas appliqués aux images renvoyées en réponse aux requêtes de miniatures ( `req=tmb`) et à certaines requêtes provenant des visionneuses Dynamic Media.

## Mise à l’échelle et alignement {#section-89ef9e5926ae438abbd8e70332749b76}

Lorsqu’un filigrane est spécifié, le serveur génère d’abord l’image composite (l’image *cible*) à laquelle le filigrane doit être appliqué (avant d’appliquer les transformations de vue). Le serveur génère ensuite l’image composite du filigrane comme n’importe quelle autre image (l’image du *filigrane*).

Contrairement aux images standard, `sizeN=` peut être spécifié pour layer=0 ou layer=comp de l’image du filigrane. Cela permet de mettre à l’échelle l’image du filigrane par rapport à l’image cible. Si `sizeN=` n’est pas spécifié, l’image du filigrane conserve sa taille en pixels lors de sa fusion avec l’image cible.

Les commandes de requête (telles que `fmt=`) et d’affichage (telles que `wid=`) sont ignorées dans les enregistrements de filigrane, à l’exception de `align=`. `align=` peut être utilisé pour positionner l’image du filigrane par rapport à l’image du filigrane par rapport à l’image cible. Cela permet de positionner le filigrane par rapport à un coin ou à un bord de l’image cible.

Après mise à l’échelle et alignement, le serveur superpose l’image du filigrane sur l’image cible à l’aide des valeurs `blendMode=` et `opac=` spécifiées pour `layer=0` ou `layer=comp` de l’image du filigrane. Enfin, les commandes request et view spécifiées pour l&#39;image cible sont appliquées pour construire l&#39;image de réponse.

Notez que l’image du filigrane ne s’étend jamais sur un espace vide ajouté à l’image de réponse par les commandes `wid=` et `hei=`.

## Exemple {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Un filigrane type peut être constitué d’une simple image RGBA contenant un logo ou un avis de copyright. Nous allons créer un enregistrement dans le catalogue d’images (ou le catalogue par défaut) avec `catalog::Id` défini sur `watermark` et spécifier le fichier image du filigrane dans `catalog::Path`. Nous voulons étirer le filigrane pour qu’il s’adapte à l’image d’affichage (sans déformer le filigrane) tout en laissant une petite marge supplémentaire, et réduire l’opacité à 20 % du filigrane d’origine. Nous avons donc défini la `catalog::Modifier` sur `sizeN=0.9,0.9&opac=20`. Pour activer le filigrane, définissez `attribute::Watermark` sur l’ID de l’entrée du catalogue de filigranes, « filigrane » dans cet exemple. Nous pourrions essayer différents choix de `blendMode=` pour obtenir différents effets d’application d’un filigrane.

## Voir aussi {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
