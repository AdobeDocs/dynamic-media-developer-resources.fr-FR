---
description: IS fournit des mécanismes pour simplifier l’utilisation des zones cliquables d’HTML. Les visionneuses JAVA et Flash dans IS incluent également une prise en charge limitée des zones cliquables.
solution: Experience Manager
title: Zones cliquables
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Zones cliquables{#image-maps}

IS fournit des mécanismes pour simplifier l’utilisation des zones cliquables d’HTML. Les visionneuses JAVA et Flash dans IS incluent également une prise en charge limitée des zones cliquables.

Les zones cliquables Source sont fournies à IS par le biais de la commande `catalog::Map` ou avec la commande `map=`, et les zones cliquables traitées sont récupérées à l’aide de la commande `req=map`.

Une zone cliquable se compose d’un ou de plusieurs éléments HTML AREA, correctement délimités par « &lt; » et « > ». Si elles sont fournies par le biais de catalog::Map, toutes les valeurs des coordonnées des pixels sont supposées être dans la résolution de l’image d’origine et relatives au coin supérieur gauche de l’image source (non modifiée). Lorsqu’elles sont fournies par le biais d’une commande `map=`, les valeurs de coordonnées sont supposées être les coordonnées du calque, par rapport au coin supérieur gauche du calque (après `rotate=` et `extend=`).

>[!NOTE]
>
>Les coordonnées de % ne sont pas autorisées à ce stade et peuvent être traitées de manière incorrecte.

IS génère une carte d&#39;image composite à partir des cartes d&#39;image sources de chaque couche constitutive en appliquant les transformations spatiales (telles que la mise à l&#39;échelle et la rotation) aux coordonnées de la carte, puis en assemblant les cartes de couche traitées dans l&#39;ordre de plan approprié (avant vers l&#39;arrière) et avec le positionnement approprié.

Les commandes suivantes sont prises en compte pour le traitement des zones cliquables lorsqu’elles sont fournies conjointement avec `req=map` (directement dans la requête, au moyen de modèles de catalogue ou dans des chaînes de `catalog::Modifier`) :

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

Toutes les autres commandes sont ignorées.

Les attributs `SHAPE` et `COORDS` d&#39;un `AREA` peuvent être modifiés pendant le traitement d&#39;une requête `req=map`, tous les autres attributs de l&#39;élément `AREA` étant transmis sans modification. Dans la plupart des cas, cela implique de modifier la valeur de `SHAPE` de `DEFAULT` à `RECT` (cela ajouterait également l’attribut `COORDS`), ou de modifier les valeurs de `COORDS`.

Tous les éléments `AREA` qui deviennent vides lors du traitement sont entièrement supprimés. Si un mappage est associé à `layer=comp`, il est placé derrière tous les autres mappages. Les données sont renvoyées sous forme de texte sous la forme d’un ou de plusieurs éléments de `AREA` HTML. Une chaîne de réponse vide indique qu’il n’existe aucune zone cliquable pour le ou les objets spécifiés.

La transparence du calque n’est pas prise en compte pour le traitement des cartes. Un calque entièrement transparent peut toujours être associé à une zone cliquable. La carte d’un calque partiellement transparent n’est pas écrêtée aux zones transparentes.

## Voir aussi {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [Spécification HTML 4.01](https://www.w3.org/TR/html401/)
