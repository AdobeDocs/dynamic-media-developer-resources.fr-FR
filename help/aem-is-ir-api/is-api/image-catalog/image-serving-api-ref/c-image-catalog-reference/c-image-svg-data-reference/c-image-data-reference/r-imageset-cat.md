---
description: Données de visionneuse d’images. Fournit un mécanisme permettant de définir des ensembles triés d’images et de contrôler les attributs utilisés par les visionneuses Dynamic Media.
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 1%

---

# ImageSet{#imageset}

Données de visionneuse d’images. Fournit un mécanisme permettant de définir des ensembles triés d’images et de contrôler les attributs utilisés par les visionneuses Dynamic Media.

Une visionneuse d’images se compose d’une liste triée d’éléments séparés par des virgules. Chaque élément se compose d’un ou de plusieurs sous-éléments (identifiants d’image, identifiants d’échantillon, chemins d’accès au fichier multimédia, libellés, etc.), séparés par des points-virgules, des deux-points ou les deux-points.

Les accolades `{ }` et les parenthèses `( )` peuvent être utilisées pour délimiter certains contenus (des valeurs de couleur, par exemple) ou indiquer des ensembles imbriqués. Les accolades ou parenthèses utilisées de cette manière ne doivent pas être codées et doivent toujours apparaître sous forme de paires correspondantes, sinon une erreur d’analyse du catalogue se produit.

>[!NOTE]
>
>Les caractères suivants sont utilisés comme délimiteurs définis et doivent être codés en HTTP lorsqu’ils apparaissent dans le jeu comme faisant partie des valeurs d’identifiant ou de chaîne :
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


Pour plus d’informations sur la structure et l’utilisation des visionneuses d’images, reportez-vous à la documentation relative aux visionneuses de serveur d’images .

Le serveur renvoie le contenu de ce champ sans modification en réponse à une requête `req=imageset`.

## Visionneuses standard {#section-5ecc8ffee7224668b63f601383665564}

Les définitions d’ensemble suivantes sont prises en charge en mode natif par le serveur d’images. L’accès à certaines visionneuses implique l’analyse, la validation et le traitement côté serveur de la visionneuse. Chaque type défini peut être identifié en spécifiant la valeur correspondante dans `catalog::AssetType`.

**Série d’échantillons de base**

Chaque élément d’un ensemble d’échantillons de base est constitué d’une référence à un enregistrement d’image et d’une référence séparée facultative à un enregistrement d’image utilisé comme échantillon.

| `*`basicSwatchSet`*` | `*`swatchItem`*&#42;[',' *`swatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageId`*[';' *`échantillon`*]` |
| `*`échantillon`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | Référence d’image IS (catalogue/id) |
| `*`swatchId`*` | Référence d’image IS (catalogue/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *`rggbb`* [ *`label`*]'}'` |
| `*`rggbb`*` | Valeur de couleur hexadécimale empilée à 6 chiffres pour les échantillons de couleur unie |
| `*`label`*` | Libellé de texte facultatif pour les échantillons de couleurs solides |

**Série d’échantillons hiérarchique**

Chaque élément d’un ensemble d’échantillons hiérarchique peut être constitué d’un élément d’échantillon de base ou d’une référence à un enregistrement d’ensemble d’échantillons (des échantillons sont nécessaires pour ces éléments).

| `*`hierarchySwatchSet`*` | `*`hierarchySwatchItem`* &#42;[ ',' *`hierarchySwatchItem`* ]` |
|---|---|
| `*`hierarchySwatchItem`*` | `*`swatchItem`* | { *`basicSwatchSetId`* ';' *`swatch`* }` |
| `*`basicSwatchSetId`*` | Référence IS (catalogue/id) à un enregistrement de catalogue définissant un ensemble d’échantillons de base |

**Visionneuses à 360° de base**

Une visionneuse à 360° de base se compose d’une simple liste d’ID d’image.

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**Visionneuses à 360° en deux dimensions**

Chaque élément d’une visionneuse à 360° bidimensionnelle peut être constitué d’une image simple, d’une référence à une visionneuse à 360° de base ou d’une visionneuse à 360° en ligne délimitée par des accolades. Les parenthèses peuvent être utilisées à la place d’accolades.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | Référence IS (catalogue/id) à un enregistrement de catalogue définissant une visionneuse à 360° de base |

**Jeux de pages**

Chaque élément d’un jeu de pages peut contenir jusqu’à trois images de page séparées par des deux-points.

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**Visionneuses de médias**

Chaque élément d’une visionneuse de médias peut être constitué d’une image, d’un ensemble d’échantillons de base, d’un ensemble d’échantillons hiérarchiques, d’une visionneuse à 360° de base, d’une visionneuse de pages ou d’une ressource vidéo. Chaque élément d’une visionneuse de médias peut également contenir un échantillon facultatif et un identifiant de type.

| `*`mediaSet`*` | `*`item`* &#42;[ , *`item`* ]` |
|---|---|
| `*`item`*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`réservé`* ] ] ]` |
| `*`videoItem`*` | `*`video`* ; *`swatchId`*` |
| `*`recutItem`*` | `*`recut`* ; *`swatchId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`swatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | Identifiant de l’image IS |
| `*`video`*` | Chemin d’accès au fichier vidéo/d’animation ou ID de catalogue statique |
| `*`recut`*` | Chemin d’accès au fichier XML de définition de récupération ou ID de catalogue statique |
| `*`imageId`*` | Identifiant de l’image IS |
| `*`setId`*` | Référence IS à une image, à une rotation ou à une visionneuse de catalogue électronique |
| `*`inlineSet`*` | Image, rotation ou visionneuse de catalogue électronique intégrée |
| `*`réservé`*` | Réservé pour une utilisation ultérieure |

**Visionneuses de vidéos**

Une visionneuse de vidéos se compose d’une simple liste d’identifiants vidéo dans laquelle chaque identifiant fait référence à une entrée dans le catalogue de contenu statique.

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## Propriétés {#section-17c731e5c46646aa90ac21f39bb693ca}

Chaîne de texte. Liste de valeurs `catalog::Id` séparées par des virgules, chemins d’accès absolus aux fichiers du serveur d’images ou chemins d’accès aux fichiers par rapport à `attribute::RootPath`. La même image peut être référencée plusieurs fois dans la visionneuse. L’enregistrement de catalogue de définition peut apparaître dans l’ensemble à n’importe quel emplacement.

Ce champ participe à la localisation de la chaîne de texte. Outre *`label`* chaînes (faisant partie de *`solidColorSpecifier`*), tous les champs délimités sont localisés s’ils contiennent au moins un jeton de localisation &#39; `^loc=…^`&#39;. Pour plus d’informations, reportez-vous à la section [Localisation de chaîne de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) dans la *référence de protocole HTTP*.

## Par défaut {#section-c3a60e360393478284f0f2d2da5b963b}

Aucune

## Voir également {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Traduction de l’ID d’objet](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [Localisation de la chaîne de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Documentation des visionneuses du serveur d’images
