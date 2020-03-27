---
description: Données de visionneuse d’images. Fournit un mécanisme permettant de définir des ensembles triés d’images et de contrôler les attributs utilisés par les visionneuses Scene7.
seo-description: Données de visionneuse d’images. Fournit un mécanisme permettant de définir des ensembles triés d’images et de contrôler les attributs utilisés par les visionneuses Scene7.
seo-title: ImageSet
solution: Experience Manager
title: ImageSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a34aaef-4053-4474-abb8-794331898d88
translation-type: tm+mt
source-git-commit: 06f227705765e4173e1c4b49dd7d8202884f5e07

---


# ImageSet{#imageset}

Données de visionneuse d’images. Fournit un mécanisme permettant de définir des ensembles triés d’images et de contrôler les attributs utilisés par les visionneuses Scene7.

Une visionneuse d’images se compose d’un d’éléments trié, séparé par des virgules, dont chaque élément se compose d’un ou de plusieurs sous-éléments (identifiants d’image, identifiants d’échantillon, chemins d’accès au fichier multimédia, libellés, etc.), séparés par des points-virgules et/ou des deux-points.

Les accolades &#39;{ }&#39; et les parenthèses &#39;( )&#39; peuvent être utilisées pour délimiter certains contenus (tels que les valeurs de couleur) ou indiquer des jeux imbriqués. Les accolades ou parenthèses utilisées de cette manière ne doivent pas être codées et doivent toujours apparaître sous forme de paires correspondantes, sinon une erreur d’analyse du catalogue se produira.

>[!NOTE]
>
>Les caractères suivants sont utilisés comme délimiteurs définis et doivent être codés en HTTP lorsqu’ils apparaissent dans le jeu comme faisant partie des valeurs d’ID ou de chaîne :
>
>* ,
>* ;
>* :
>* {
>* }
>* (
>* )



Pour plus d’informations sur la structure et l’utilisation des visionneuses d’images, reportez-vous à la documentation des visionneuses de diffusion d’images.

Le serveur renvoie le contenu de ce champ sans modification en réponse à une `req=imageset` demande.

## Jeux standard {#section-5ecc8ffee7224668b63f601383665564}

Les définitions d’ensemble suivantes sont prises en charge en mode natif par Image Serving et l’accès à certaines visionneuses implique l’analyse, la validation et le traitement côté serveur de la visionneuse. Chaque type de jeu peut être identifié en spécifiant la valeur correspondante dans `catalog::AssetType`.

**Séries d’échantillons de base**

Chaque élément d’une série d’échantillons de base est constitué d’une référence à un enregistrement d’image et d’une référence distincte facultative à un enregistrement d’image utilisé comme échantillon.

| ` *`basicSwatchSet`*` | ` *``*&#42;[',' *`swatchItemswatchItem`*]` |
|---|---|
| ` *`swatchItem`*` | ` *``*[';' *`imageIdswatch`*]` |
| ` *`nuance`*` | ` *`swatchId`*|solidColorSpecifier` |
| ` *`imageId`*` | Référence de l’image IS (catalogue/id) |
| ` *`swatchId`*` | Référence de l’image IS (catalogue/id) |
| ` *`solidColorSpecifier`*` | ` '{0x' *``* [ *`rggbblabel`*]'}'` |
| ` *`rrggbb`*` | Valeur de couleur RVB hexadécimale empilée à 6 chiffres pour les nuances de couleur unie |
| ` *`label`*` | Libellé de texte facultatif pour les nuances de couleur unie |

**Séries d’échantillons hiérarchiques**

Chaque élément d’une série d’échantillons hiérarchique peut se composer d’un élément d’échantillon de base ou d’une référence à un enregistrement d’ensemble d’échantillons (des échantillons sont nécessaires pour ces éléments).

| ` *`hierarchySwatchSet`*` | ` *``* &#42;[ ',' *`hierarchySwatchItemHiérarchicalSwatchItem`* ]` |
|---|---|
| ` *`hierarchySwatchItem`*` | ` *``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| ` *`basicSwatchSetId`*` | Référence IS (catalogue/id) à un enregistrement de catalogue définissant une visionneuse d’échantillons de base |

**Visionneuses à 360° de base**

Une visionneuse à 360° de base se compose d’un simple d’ID d’image.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**Visionneuses à 360° bidimensionnelles**

Chaque élément d’une visionneuse à 360° bidimensionnelle peut être constitué d’une image simple, d’une référence à une visionneuse à 360° de base ou d’une visionneuse à 360° en ligne délimitée par des accolades. Les parenthèses peuvent être utilisées à la place des accolades.

| ` *`2dSpinItem`*` | ` *`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| ` *`2dSpinItem`*` | ` *``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| ` *`basicSpinSetId`*` | Référence IS (catalogue/id) à un enregistrement de catalogue définissant une visionneuse à 360° de base |

**Jeux de pages**

Chaque élément d’un jeu de pages peut comporter jusqu’à trois images de page séparées par des deux-points.

| ` *`pageSet`*` | ` *``* &#42;[ , *`pageImageItem`* ]` |
|---|---|
| ` *`pageItem`*` | ` *``* [ : *``* [ : *`imageImageIdimageId`* ] ]` |

**Visionneuses de supports**

Chaque élément d’une visionneuse de supports peut se composer d’une image, d’une visionneuse d’échantillons de base, d’une série d’échantillons hiérarchique, d’une visionneuse à 360° de base, d’une visionneuse à 360° bidimensionnelle, d’une visionneuse de pages ou d’un fichier vidéo. Chaque élément de visionneuse de supports peut également contenir une nuance et un identifiant de type facultatifs.

| ` *`mediaSet`*` | ` *``* &#42;[ , *`item`* ]` |
|---|---|
| ` *`élément`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemrecutImageItemsetItemIDreserved`* ] ] ]` |
| ` *`videoItem`*` | ` *``* ; *`videoswatchId`*` |
| ` *`recutItem`*` | ` *``* ; *`recutswatchId`*` |
| ` *`imageItem`*` | ` *``* ; [ *`imageIdswatchId`* ]` |
| ` *`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| ` *`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| ` *`swatchId`*` | ID image IS |
| ` *`video`*` | Chemin du fichier vidéo/animation ou ID de catalogue statique |
| ` *`découper`*` | Chemin d’accès au fichier XML de définition de découpe ou ID de catalogue statique |
| ` *`imageId`*` | ID image IS |
| ` *`setId`*` | Référence IS à l’image, à la rotation ou à la visionneuse d’ecatalog |
| ` *`inlineSet`*` | Image, rotation ou visionneuse de catalogue en ligne |
| ` *`réservé`*` | Réservé pour une utilisation ultérieure |

**Visionneuses de vidéos**

Une visionneuse de vidéos se compose d’un simple d’identifiants vidéo dans lequel chaque ID référence une entrée dans le catalogue de contenu statique.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## Propriétés {#section-17c731e5c46646aa90ac21f39bb693ca}

Chaîne de texte. de `catalog::Id` valeurs séparées par des virgules, chemins d’accès absolus aux fichiers du serveur d’images ou chemins d’accès aux fichiers par rapport à `attribute::RootPath`. La même image peut être référencée plusieurs fois dans la visionneuse. L’enregistrement de catalogue de définition peut apparaître dans le jeu à n’importe quel emplacement.

Ce champ participe aux  de chaîne de texte. Outre *`label`* les chaînes (partie de la *`solidColorSpecifier`*), tous les champs délimités sont localisés s’ils contiennent au moins un jeton de  de `^loc=…^`&#39;. Pour plus d’informations, reportez-vous à la [Chaîne de](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) texte *dans le Guide de référence* du protocoleHTTP.

## Par défaut {#section-c3a60e360393478284f0f2d2da5b963b}

Aucune

## Voir également {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribut::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), Traduction [d’ID](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) d’objet, chaînes de [](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) texte, documentation des visionneuses de diffusion d’images
