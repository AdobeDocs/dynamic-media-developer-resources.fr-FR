---
description: Données de visionneuse d’images. Fournit un mécanisme permettant de définir des jeux triés d’images et des attributs de contrôle utilisés par les visionneuses Dynamic Media.
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 2%

---


# ImageSet{#imageset}

Données de visionneuse d’images. Fournit un mécanisme permettant de définir des jeux triés d’images et des attributs de contrôle utilisés par les visionneuses Dynamic Media.

Une visionneuse d’images se compose d’une liste d’éléments triée, séparée par des virgules, chaque élément se composant d’un ou de plusieurs sous-éléments (identifiants d’image, identifiants d’échantillon, chemins d’accès aux fichiers multimédias, libellés, etc.), séparés par des points-virgules et/ou des deux-points.

Les accolades `{ }` et les parenthèses `( )` peuvent être utilisées pour délimiter certains contenus (tels que les valeurs de couleur) ou indiquer des jeux imbriqués. Les accolades ou parenthèses utilisées de cette façon ne doivent pas être codées et doivent toujours apparaître sous forme de paires correspondantes, sinon une erreur d&#39;analyse du catalogue se produit.

>[!NOTE]
>
>Les caractères suivants sont utilisés comme délimiteurs définis et doivent être codés en HTTP lorsqu’ils apparaissent dans l’ensemble comme faisant partie des valeurs d’id ou de chaîne :
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



Pour plus d’informations sur la structure et l’utilisation des visionneuses d’images, reportez-vous à la documentation des visionneuses d’images.

Le serveur renvoie le contenu de ce champ sans modification en réponse à une demande `req=imageset`.

## Jeux de normes {#section-5ecc8ffee7224668b63f601383665564}

Les définitions de visionneuse suivantes sont prises en charge en mode natif par Image Serving et l’accès avec certaines visionneuses implique l’analyse, la validation et le traitement côté serveur de la visionneuse. Chaque type de jeu peut être identifié en spécifiant la valeur correspondante dans `catalog::AssetType`.

**Série d’échantillons de base**

Chaque élément d’une série d’échantillons de base est constitué d’une référence à un enregistrement d’image et d’une référence distincte facultative à un enregistrement d’image utilisé comme échantillon.

| `*`basicSwatchSet`*` | `*``*&#42;[',' *`swatchItemswatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*``*[';' *`imageIdswatch`*]` |
| `*`nuance`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | Référence d’image IS (catalogue/id) |
| `*`swatchId`*` | Référence d’image IS (catalogue/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *``* [ *`rgbblabel`*]'}'` |
| `*`rrggbb`*` | Valeur de couleur RVB hexadécimale à 6 chiffres empilée pour les nuances de couleur unie |
| `*`label`*` | Libellé de texte facultatif pour les nuances de couleur unie |

**Séries d’échantillons hiérarchiques**

Chaque élément d’une série d’échantillons hiérarchique peut être constitué d’un élément d’échantillon de base ou d’une référence à un enregistrement d’ensemble d’échantillons (des échantillons sont requis pour ces éléments).

| `*`hierarchySwatchSet`*` | `*``* &#42;[ ',' *`hierarchySwatchItemhierarchySwatchItem`* ]` |
|---|---|
| `*`hierarchySwatchItem`*` | `*``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| `*`basicSwatchSetId`*` | Référence IS (catalogue/id) à un enregistrement de catalogue définissant une série d’échantillons de base |

**Visionneuses à 360° de base**

Une visionneuse à 360° de base se compose d’une simple liste d’ID d’image.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**Visionneuses à 360° bidimensionnelles**

Chaque élément d’une visionneuse à 360° bidimensionnelle peut être constitué d’une image simple, d’une référence à une visionneuse à 360° de base ou d’une visionneuse à 360° de base en ligne délimitée par des accolades. Les parenthèses peuvent être utilisées à la place des accolades.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| `*`basicSpinSetId`*` | Référence IS (catalogue/id) à un enregistrement de catalogue définissant une visionneuse à 360° de base |

**Jeux de pages**

Chaque élément d’un jeu de pages peut comporter jusqu’à trois images de page séparées par des deux-points.

| `*`pageSet`*` | `*``* &#42;[ , *`pageImageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*``* [ : *``* [ : *`imageIdimageIdimageId`* ] ]` |

**Visionneuses de supports**

Chaque élément d’une visionneuse de supports peut se composer d’une image, d’une visionneuse d’échantillons de base, d’une visionneuse d’échantillons hiérarchique, d’une visionneuse à 360° de base, d’une visionneuse à 360° bidimensionnelle, d’une visionneuse de pages ou d’une ressource vidéo. Chaque élément de visionneuse de supports peut également contenir une nuance et un identifiant de type facultatifs.

| `*`mediaSet`*` | `*``* &#42;[ , *`itemitem`* ]` |
|---|---|
| `*`élément`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemrecutItemimageItemsetItemIDreserved`* ] ] ]` |
| `*`videoItem`*` | `*``* ; *`videoswatchId`*` |
| `*`recutItem`*` | `*``* ; *`recutswatchId`*` |
| `*`imageItem`*` | `*``* ; [ *`imageIdswatchId`* ]` |
| `*`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | ID d’image IS |
| `*`video`*` | Chemin du fichier vidéo/animation ou ID de catalogue statique |
| `*`découper`*` | Chemin d’accès au fichier XML de définition de découpe ou ID de catalogue statique |
| `*`imageId`*` | ID d’image IS |
| `*`setId`*` | Référence IS à l’image, à la rotation ou à la visionneuse de catalogues électroniques |
| `*`inlineSet`*` | Image, rotation ou visionneuse de catalogue électronique insérée |
| `*`réservé`*` | Réservé pour une utilisation ultérieure |

**Visionneuses de vidéos**

Une visionneuse de vidéos se compose d’une simple liste d’identifiants vidéo dans laquelle chaque identifiant référence une entrée dans le catalogue de contenu statique.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## Propriétés {#section-17c731e5c46646aa90ac21f39bb693ca}

Chaîne de texte. Liste séparée par des virgules de valeurs `catalog::Id`, de chemins d’accès aux fichiers du serveur d’images absolus ou de chemins d’accès aux fichiers par rapport à `attribute::RootPath`. La même image peut être référencée plusieurs fois dans la visionneuse. L’enregistrement de catalogue de définition peut apparaître dans l’ensemble à n’importe quel emplacement.

Ce champ participe à la localisation des chaînes de texte. Outre les chaînes *`label`* (faisant partie de *`solidColorSpecifier`*), tous les champs délimités sont localisés s’ils contiennent au moins un jeton de localisation &#39; `^loc=…^`&#39;. Pour plus d&#39;informations, consultez la [Localisation de chaînes de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) dans le *Guide de référence du protocole HTTP*.

## Par défaut {#section-c3a60e360393478284f0f2d2da5b963b}

Aucune

## Voir également {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), Traduction [ de l’ID ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) d’objet, Localisation [ de chaîne de ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) texte, documentation des visionneuses de diffusion d’images
