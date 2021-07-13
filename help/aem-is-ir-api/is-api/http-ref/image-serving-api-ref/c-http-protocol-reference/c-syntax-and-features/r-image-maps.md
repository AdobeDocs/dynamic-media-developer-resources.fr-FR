---
description: IS fournit des mécanismes pour simplifier l’utilisation des zones cliquables HTML. Les visionneuses JAVA et par Flash dans IS incluent également une prise en charge limitée des zones cliquables.
solution: Experience Manager
title: Cartes d’images
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Cartes d’images{#image-maps}

IS fournit des mécanismes pour simplifier l’utilisation des zones cliquables HTML. Les visionneuses JAVA et par Flash dans IS incluent également une prise en charge limitée des zones cliquables.

Les zones cliquables sources sont fournies à IS via `catalog::Map` ou avec la commande `map=` et les zones cliquables sont récupérées à l’aide de la commande `req=map`.

Une zone cliquable se compose d’un ou de plusieurs éléments de zone HTML, délimités de manière appropriée par &quot;&lt;&quot; et &quot;>&quot;. Si elles sont fournies par catalog::Map, toutes les valeurs de coordonnées en pixels sont supposées se trouver dans la résolution de l’image d’origine et relatives par rapport au coin supérieur gauche de l’image source (non modifiée). Lorsqu’elles sont fournies via une commande `map=`, les valeurs de coordonnées sont supposées être des coordonnées de calque, par rapport au coin supérieur gauche du calque (après `rotate=` et `extend=`).

>[!NOTE]
>
>Les coordonnées % ne sont pas autorisées pour le moment et peuvent être traitées incorrectement.

IS génère une zone cliquable composite à partir des zones cliquables source de chaque couche constituante en appliquant les transformations spatiales (telles que la mise à l’échelle et la rotation) aux coordonnées de la carte, puis en assemblant les zones cliquables traitées dans l’ordre z approprié (avant vers l’arrière) et avec le positionnement approprié.

Les commandes suivantes sont prises en compte pour le traitement de la zone cliquable lorsqu’elles sont fournies conjointement avec `req=map` (directement dans la requête, via des modèles de catalogue ou dans des chaînes `catalog::Modifier`) :

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

Les attributs `SHAPE` et `COORDS` d&#39;un `AREA` peuvent être modifiés lors du traitement d&#39;une requête `req=map`, tous les autres attributs de l&#39;élément `AREA` sont transmis sans modification. Dans la plupart des cas, cela implique de modifier la valeur `SHAPE` de `DEFAULT` en `RECT` (cela ajouterait également l’attribut `COORDS`) ou de modifier les valeurs `COORDS`.

Tous les éléments `AREA` qui deviennent vides pendant le traitement seront entièrement supprimés. Si une carte est associée à `layer=comp`, elle est placée derrière toutes les autres cartes. Les données sont renvoyées sous forme de texte un ou plusieurs éléments HTML `AREA`. Une chaîne de réponse vide indique qu’il n’existe aucune zone cliquable pour le ou les objets spécifiés.

La transparence des calques n’est pas prise en compte pour le traitement des cartes. Un calque entièrement transparent peut toujours être associé à une zone cliquable. La carte d’un calque partiellement transparent ne sera pas tronquée dans les régions transparentes.

## Voir aussi {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [catalogue::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md),  [HTML 4.01 Specification](http://www.w3.org/TR/html401/)
