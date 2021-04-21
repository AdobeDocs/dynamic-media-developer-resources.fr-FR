---
description: IS fournit des mécanismes pour simplifier l’utilisation des zones cliquables HTML. Les lecteurs basés sur JAVA et sur Flash dans IS incluent également une prise en charge limitée des zones cliquables.
solution: Experience Manager
title: Zones cliquables
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Mappages d’images{#image-maps}

IS fournit des mécanismes pour simplifier l’utilisation des zones cliquables HTML. Les lecteurs basés sur JAVA et sur Flash dans IS incluent également une prise en charge limitée des zones cliquables.

Les zones cliquables source sont fournies à IS par `catalog::Map` ou avec la commande `map=`, et les zones traitées sont récupérées à l&#39;aide de la commande `req=map`.

Une zone cliquable se compose d’un ou de plusieurs éléments de zone HTML, délimités correctement par &quot;&lt;&quot; et &quot;>&quot;. Si elles sont fournies par catalog::Map, toutes les valeurs de coordonnées de pixels sont supposées se trouver dans la résolution d’image d’origine et relatives au coin supérieur gauche de l’image source (non modifiée). Lorsqu&#39;elles sont fournies par une commande `map=`, les valeurs de coordonnées sont supposées être des coordonnées de calque, par rapport au coin supérieur gauche du calque (après `rotate=` et `extend=`).

>[!NOTE]
>
>Les coordonnées % ne sont pas autorisées pour le moment et peuvent être traitées incorrectement.

IS génère une zone cliquable composite à partir des zones cliquables source de chaque calque constituant en appliquant les transformations spatiales (telles que la mise à l’échelle et la rotation) aux coordonnées de la zone cliquable, puis en assemblant les zones calquées traitées dans l’ordre z approprié (avant à arrière) et avec le positionnement approprié.

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

Toutes les autres commandes sont ignorées.

Les attributs `SHAPE` et `COORDS` d&#39;un `AREA` peuvent être modifiés lors du traitement d&#39;une demande `req=map`, tous les autres attributs de l&#39;élément `AREA` sont transmis sans modification. Dans la plupart des cas, cela implique de changer la valeur `SHAPE` de `DEFAULT` en `RECT` (cela ajouterait également l&#39;attribut `COORDS`) ou de modifier les valeurs `COORDS`.

Tout élément `AREA` qui devient vide pendant le traitement sera entièrement supprimé. Si une carte est associée à `layer=comp`, elle est placée derrière toutes les autres cartes. Les données sont renvoyées sous la forme d’un texte sous forme d’éléments HTML `AREA` ou plus. Une chaîne de réponse vide indique qu’il n’existe aucune carte d’image pour le ou les objets spécifiés.

La transparence des calques n’est pas prise en compte pour le traitement des mappages. Un calque entièrement transparent peut toujours être associé à une zone cliquable. La carte d’un calque partiellement transparent ne sera pas coupée dans les zones transparentes.

## Voir aussi {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md),  [HTML 4.01 Specification](http://www.w3.org/TR/html401/)
