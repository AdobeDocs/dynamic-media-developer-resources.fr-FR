---
description: IS fournit des mécanismes pour simplifier l’utilisation des zones cliquables HTML. Les visionneuses JAVA et Flash de IS incluent également une prise en charge limitée des zones cliquables.
seo-description: IS fournit des mécanismes pour simplifier l’utilisation des zones cliquables HTML. Les visionneuses JAVA et Flash de IS incluent également une prise en charge limitée des zones cliquables.
seo-title: Mappages d’images
solution: Experience Manager
title: Mappages d’images
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# Image maps{#image-maps}

IS fournit des mécanismes pour simplifier l’utilisation des zones cliquables HTML. Les visionneuses JAVA et Flash de IS incluent également une prise en charge limitée des zones cliquables.

Les zones cliquables source sont fournies à IS via `catalog::Map` ou avec la `map=` commande, et les zones traitées sont récupérées à l’aide de la `req=map` commande.

Une zone cliquable se compose d’un ou de plusieurs éléments de zone HTML, délimités correctement par &quot;&lt;&quot; et &quot;>&quot;. Si elles sont fournies via catalog::Map, toutes les valeurs de coordonnées de pixels sont supposées figurer dans la résolution d’image d’origine et relatives au coin supérieur gauche de l’image source (non modifiée). Lorsqu’elles sont fournies par le biais d’une `map=` commande, les valeurs de coordonnées sont supposées être des coordonnées de calque, par rapport au coin supérieur gauche du calque (après `rotate=` et `extend=`).

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Les coordonnées % ne sont pas autorisées pour le moment et peuvent être traitées incorrectement.

IS génère une zone cliquable composite à partir des zones cliquables source de chaque calque constitutif en appliquant les transformations spatiales (telles que la mise à l’échelle et la rotation) aux coordonnées de la zone cliquable, puis en assemblant les zones de calque traitées dans l’ordre z approprié (de l’avant vers l’arrière) et avec le positionnement approprié.

Les commandes suivantes sont prises en compte pour le traitement de la zone cliquable lorsqu’elles sont fournies conjointement avec `req=map` (directement dans la requête, via des modèles de catalogue ou dans des `catalog::Modifier` chaînes) :

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

Les attributs `SHAPE` et `COORDS` d’un `AREA` élément peuvent être modifiés lors du traitement d’une `req=map` demande. Tous les autres attributs de l’ `AREA` élément sont transmis sans modification. Dans la plupart des cas, cela implique de changer la `SHAPE` valeur `DEFAULT` en `RECT` (cela ajouterait également l’ `COORDS` attribut) ou de modifier les `COORDS` valeurs.

Les `AREA` éléments qui deviennent vides pendant le traitement seront entièrement supprimés. Si une carte est associée à `layer=comp` elle est placée derrière toutes les autres cartes. Les données sont renvoyées sous forme de texte 1 sous forme d’éléments HTML `AREA` . Une chaîne de réponse vide indique qu’il n’existe aucune zone cliquable pour le ou les objets spécifiés.

La transparence des calques n’est pas prise en compte pour le traitement de la carte. Un calque entièrement transparent peut toujours être associé à une zone cliquable. La carte d’un calque partiellement transparent ne sera pas tronquée dans les zones transparentes.

## Voir aussi {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), spécification [HTML 4.01](http://www.w3.org/TR/html401/)
