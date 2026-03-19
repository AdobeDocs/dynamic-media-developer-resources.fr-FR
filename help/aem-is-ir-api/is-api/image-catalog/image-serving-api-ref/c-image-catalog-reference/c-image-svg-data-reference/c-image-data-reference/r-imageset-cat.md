---
description: Données de visionneuse d’images. Fournit un mécanisme pour définir des ensembles triés d’images et des attributs de contrôle utilisés par les visionneuses Dynamic Media.
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 1%

---

# ImageSet{#imageset}

Données de visionneuse d’images. Fournit un mécanisme pour définir des ensembles triés d’images et des attributs de contrôle utilisés par les visionneuses Dynamic Media.

Une visionneuse d’images se compose d’une liste d’éléments triés séparés par des virgules. Chaque élément se compose d’un ou de plusieurs sous-éléments (identifiants d’image, identifiants d’échantillon, chemins d’accès aux fichiers multimédias, libellés, etc.), séparés par des points-virgules, des deux-points, ou les deux.

Les accolades `{ }` et les parenthèses `( )` peuvent être utilisées pour délimiter certains contenus (comme les valeurs de couleur) ou indiquer des ensembles imbriqués. Les accolades ou les parenthèses utilisées de cette manière ne doivent pas être codées et doivent toujours apparaître comme des paires correspondantes, sinon une erreur d’analyse du catalogue se produit.

>[!NOTE]
>
>Les caractères suivants sont utilisés comme délimiteurs de jeu et doivent être codés en HTTP lorsqu’ils apparaissent dans le jeu comme partie des valeurs d’identifiant ou de chaîne :
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


Reportez-vous à la documentation Visionneuses d’hébergements d’images pour plus d’informations sur la structure et l’utilisation des visionneuses d’images.

Le serveur renvoie le contenu de ce champ sans modification en réponse à une requête `req=imageset`.

## Ensembles standard {#section-5ecc8ffee7224668b63f601383665564}

Les définitions d’ensemble suivantes sont prises en charge de manière native par le service d’images et l’accès avec certaines visionneuses implique l’analyse, la validation et le traitement de la visionneuse côté serveur. Chaque type d’ensemble peut être identifié en spécifiant la valeur correspondante dans `catalog::AssetType`.

**Échantillons de base**

Chaque élément d’un ensemble d’échantillons de base se compose d’une référence à un enregistrement d’image et d’une référence distincte facultative à un enregistrement d’image utilisé comme échantillon.

| `*`basicSwatchSet`*` | `*`swatchItem`*&#42;[',' *`swatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageId`*[';' *`swatch`*]` |
| `*`nuancier`*` | `*`swatchId`*`\|`solidColorSpecifier` |
| `*`imageId`*` | Référence de l’image IS (catalogue/id) |
| `*`swatchId`*` | Référence de l’image IS (catalogue/id) |
| `*`solideColorSpecifier`*` | ` '{0x' *`rrggbb`* [ *`label`*]'}'` |
| `*`rrggbb`*` | Valeur de couleur RGB hexadécimale à 6 chiffres empaquetée pour les échantillons de couleurs unies |
| `*`label`*` | Libellé de texte facultatif pour les échantillons de couleurs unies |

**Échantillons hiérarchiques**

Chaque élément d’un jeu d’échantillons hiérarchique peut être constitué d’un élément d’échantillon de base ou d’une référence à un enregistrement de jeu d’échantillons (des échantillons sont requis pour ces éléments).

| `*`hiérarchicalSwatchSet`*` | `*`hierarchySwatchItem`* &#42;[ ',' *`hierarchySwatchItem`* ]` |
|---|---|
| `*`hierarchySwatchItem`*` | `*`swatchItem`*` \| `{` *`basicSwatchSetId`* &#39;;&#39; *`swatch`* `}` |
| `*`basicSwatchSetId`*` | Référence IS (catalog/id) à un enregistrement de catalogue définissant un ensemble de nuanciers de base |

**Visionneuses à 360°De base**

Une visionneuse à 360° de base se compose d’une simple liste d’identifiants d’image.

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**Visionneuses à 360°**

Chaque élément d’une visionneuse à 360° bidimensionnelle peut être constitué d’une image simple, d’une référence à une visionneuse à 360° de base ou d’une visionneuse à 360° de base en ligne délimitée par des accolades. Les parenthèses peuvent être utilisées à la place des accolades.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`*` \| `{` &#39;{&#39; *`basicSpinSet`* &#39;}&#39; `}` \| `*`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | Référence IS (catalog/id) à un enregistrement de catalogue définissant une visionneuse à 360° de base |

**Ensembles de pages**

Chaque élément d’un ensemble de pages peut se composer d’images de trois pages au maximum, séparées par des deux-points.

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**Visionneuses de médias**

Chaque élément d’une visionneuse de médias peut être constitué d’une image, d’une visionneuse de base, d’une visionneuse hiérarchique, d’une visionneuse à 360° de base, d’une visionneuse à 360° bidimensionnelle, d’une visionneuse de pages ou d’une ressource vidéo. Chaque élément de visionneuse de médias peut également contenir un échantillon facultatif et un identifiant de type.

| `*`mediaSet`*` | `*`item`* &#42;[ , *`item`* ]` |
|---|---|
| `*`item`*` | `{ *`videoItem`*` \| *`recutItem`* * *`imageItem`*`}}`**`setItem`*`}` `[` ; `[`*`ID`*`]` `[` ; `[`*`reserved`*`] ] ]` |
| `*`videoItem`*` | `*`video`* ; *`swatchId`*` |
| `*`recutItem`*` | `*`recut`* ; *`swatchId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | `{ *`setId`*` \| `{` &#39;{&#39; *`inlineSet`* &#39;}&#39; `} }` ; *`swatchId`* |
| `*`ID`*` | `media type identifier` `[` img \| \| simple advanced_image \| img \| img_set \| advanced_imageset \| advanced_swatchset \| spin \| `]` vidéo |
| `*`swatchId`*` | Identifiant de l’image IS |
| `*`vidéo`*` | Chemin d’accès au fichier vidéo/d’animation ou identifiant de catalogue statique |
| `*`recut`*` | Chemin d’accès du fichier XML de définition de recuperation ou ID de catalogue statique |
| `*`imageId`*` | Identifiant de l’image IS |
| `*`setId`*` | Référence IS à une image, une rotation ou un ensemble de catalogue électronique |
| `*`inlineSet`*` | Image intégrée, rotation ou ensemble de catalogue électronique |
| `*`réservé`*` | Réservé à un usage ultérieur |

**Visionneuses de vidéos**

Une visionneuse de vidéos est constituée d’une simple liste d’identifiants vidéo, où chaque identifiant fait référence à une entrée du catalogue de contenu statique.

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## Propriétés {#section-17c731e5c46646aa90ac21f39bb693ca}

Chaîne de texte. Liste séparée par des virgules de valeurs de `catalog::Id`, de chemins d’accès absolus aux fichiers du serveur d’images ou de chemins d’accès relatifs à `attribute::RootPath`. La même image peut être référencée plusieurs fois dans la visionneuse. L’enregistrement de catalogue de définition peut apparaître dans le jeu à n’importe quel emplacement.

Ce champ participe à la localisation de la chaîne de texte. En plus des chaînes *`label`* (qui font partie du *`solidColorSpecifier`*), tous les champs délimités sont localisés s’ils incluent au moins un jeton de localisation « `^loc=…^` ». Pour plus d’informations[ consultez la section ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)Localisation de chaîne de texte dans la section *Référence du protocole HTTP*.

## Par défaut {#section-c3a60e360393478284f0f2d2da5b963b}

Aucune

## Voir également {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Object Id Translation](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Documentation des visionneuses de diffusion d’images
