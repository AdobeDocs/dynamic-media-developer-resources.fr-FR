---
description: IS fournit des mécanismes pour simplifier l’utilisation des zones cliquables de HTML. Les visionneuses JAVA et par Flash dans IS incluent également une prise en charge limitée des zones cliquables.
solution: Experience Manager
title: Cartes d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Cartes d’images{#image-maps}

IS fournit des mécanismes pour simplifier l’utilisation des zones cliquables de HTML. Les visionneuses JAVA et par Flash dans IS incluent également une prise en charge limitée des zones cliquables.

Les zones cliquables source sont fournies à IS via `catalog::Map` ou avec la fonction `map=` et les mappages traités sont récupérés à l’aide de la commande `req=map` .

Une zone cliquable se compose d’un ou de plusieurs éléments de zone de HTML, délimités de manière appropriée par &quot;&lt;&quot; et &quot;>&quot;. Si elles sont fournies par catalog::Map, toutes les valeurs de coordonnées en pixels sont supposées se trouver dans la résolution de l’image d’origine et relatives par rapport au coin supérieur gauche de l’image source (non modifiée). Lorsqu’il est fourni via un `map=` , les valeurs de coordonnée sont supposées être des coordonnées de calque, par rapport au coin supérieur gauche du calque (après `rotate=` et `extend=`).

>[!NOTE]
>
>Les coordonnées % ne sont pas autorisées pour le moment et peuvent être traitées incorrectement.

IS génère une zone cliquable composite à partir des zones cliquables source de chaque couche constituante en appliquant les transformations spatiales (telles que la mise à l’échelle et la rotation) aux coordonnées de la carte, puis en assemblant les zones cliquables traitées dans l’ordre z approprié (avant vers l’arrière) et avec le positionnement approprié.

Les commandes suivantes sont prises en compte pour le traitement de la zone cliquable lorsqu’elles sont fournies conjointement avec `req=map` (directement dans la requête, via des modèles de catalogue, ou dans `catalog::Modifier` chaînes) :

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

Toutes les autres commandes sont effectivement ignorées.

Le `SHAPE` et `COORDS` attributs d’un `AREA` peut être modifié lors du traitement d’une `req=map` requête, tous les autres attributs de la fonction `AREA` sont transmis sans modification. Dans la plupart des cas, cela implique de modifier la variable `SHAPE` de `DEFAULT` to `RECT` Cela ajouterait également la variable `COORDS` ) ou en modifiant la variable `COORDS` valeurs.

Quelconque `AREA` les éléments qui deviennent vides lors du traitement sont entièrement supprimés. Si une map est associée à `layer=comp` il est placé derrière toutes les autres cartes. Les données sont renvoyées sous forme texte un par HTML ou plus. `AREA` éléments . Une chaîne de réponse vide indique qu’il n’existe aucune zone cliquable pour le ou les objets spécifiés.

La transparence des calques n’est pas prise en compte pour le traitement des cartes. Un calque entièrement transparent peut toujours être associé à une zone cliquable. La carte d’un calque partiellement transparent ne sera pas tronquée dans les régions transparentes.

## Voir aussi {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalogue : Carte](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [Spécification du HTML 4.01](https://www.w3.org/TR/html401/)
