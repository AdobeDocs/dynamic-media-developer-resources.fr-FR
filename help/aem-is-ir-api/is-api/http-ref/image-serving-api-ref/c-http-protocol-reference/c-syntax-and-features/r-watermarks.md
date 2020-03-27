---
description: Image Serving implémente un filigrane visuel simple.
seo-description: Image Serving implémente un filigrane visuel simple.
seo-title: Filigranes
solution: Experience Manager
title: Filigranes
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Filigranes{#watermarks}

Image Serving implémente un filigrane visuel simple.

Un filigrane est généralement une image semi-transparente, mais il peut s’agir d’un texte ou d’une image composite superposée plus complexe. Une fois que tous les attributs de  de ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) ont été appliqués, le serveur placera le filigrane sur l’image de réponse.

Le filigrane est activé en définissant une entrée `attribute::Watermark` de catalogue valide qui contiendrait l’image ou le modèle de filigrane. Si `attribute::Watermark` est défini dans un catalogue nommé, le serveur ajoute le filigrane à toutes les demandes d’image qui référencent l’ID de catalogue dans l’URL de requête. Si `default::Watermark` est défini (dans le catalogue par défaut [!DNL default.ini]), le filigrane est appliqué à toutes les demandes d’image, qu’elles fassent référence à un catalogue ou non.

Les filigranes ne sont pas appliqués aux images renvoyées en réponse aux requêtes de miniature ( `req=tmb`) et à certaines requêtes des visionneuses Scene7.

## Mise à l’échelle et alignement {#section-89ef9e5926ae438abbd8e70332749b76}

Lorsqu’un filigrane est spécifié, le serveur génère d’abord l’image composite (l’image **) à laquelle le filigrane doit être appliqué (avant d’appliquer les  de). Le serveur génère ensuite l’image composite pour le filigrane, comme toute autre image (image *de* filigrane).

Contrairement aux images standard, `sizeN=` vous pouvez spécifier layer=0 ou layer=comp de l’image du filigrane. Cela permet de mettre à l’échelle l’image du filigrane par rapport à l’image  du. Si elle `sizeN=` n’est pas spécifiée, l’image du filigrane conserve sa taille en pixels lors de la fusion avec l’image  du.

Les commandes de requête (par exemple `fmt=`) et les commandes de  (par exemple `wid=`) sont ignorées dans les enregistrements de filigrane, à l’exception de `align=`. `align=` peut être utilisé pour positionner l’image du filigrane par rapport à l’image du filigrane par rapport à l’image  du. Cela permet de positionner le filigrane par rapport à un angle ou à un bord de l’image .

Une fois la mise à l’échelle et l’alignement effectués, le serveur superpose l’image du filigrane sur l’image  à l’aide des `blendMode=` valeurs et `opac=` spécifiées pour `layer=0` ou `layer=comp` de l’image du filigrane. Enfin, les commandes de requête et de  de spécifiées pour l’image  sont appliquées pour construire l’image de réponse.

Notez que l’image du filigrane ne s’étend jamais sur un espace vide ajouté à l’image de réponse par les `wid=` commandes et `hei=` .

## Exemple {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Un filigrane type peut être constitué d’une image RGBA simple contenant un logo ou une mention de copyright. Nous créons un enregistrement dans le catalogue d’images (ou le catalogue par défaut) avec la `catalog::Id` valeur `watermark` et spécifions le fichier image du filigrane dans `catalog::Path`. Nous voulons étirer le filigrane pour l&#39;adapter à l&#39;image  (sans déformer le filigrane) tout en laissant une marge supplémentaire, et réduire l&#39;opacité à 20% du filigrane d&#39;origine, donc nous nous mettons `catalog::Modifier` à `sizeN=0.9,0.9&opac=20`. Pour activer le filigrane, définissez l’ID `attribute::Watermark` de l’entrée du catalogue de filigranes, &quot;filigrane&quot; dans cet exemple. Nous pourrions faire des expériences avec différents `blendMode=` choix pour obtenir différents effets de filigrane.

## Voir aussi {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribut:Filigrane](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
