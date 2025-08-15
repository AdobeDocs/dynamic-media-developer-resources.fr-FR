---
description: Données de la visionneuse d’images. Fournit un mécanisme permettant de définir des ensembles triés d’images et des attributs de contrôle utilisés par les Dynamic Media les visionneuses.
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

Données de la visionneuse d’images. Fournit un mécanisme permettant de définir des ensembles triés d’images et des attributs de contrôle utilisés par les Dynamic Media les visionneuses.

Une visionneuse d’images se compose d’une liste d’éléments triés et séparés par des virgules. Chaque élément se compose d’un ou plusieurs sous-éléments (ID d’image, ID d’échantillon, chemins d’accès aux fichiers multimédias, étiquettes, etc.), séparés par des points-virgules, deux-points ou les deux.

Des accolades `{ }` et des parenthèses `( )` peuvent être utilisées pour délimiter certains contenus (tels que les valeurs de couleur) ou indiquer des ensembles imbriqués. Les accolades ou parenthèses utilisées de cette manière ne doivent pas être codées et doivent toujours apparaître comme des paires correspondantes, sinon une erreur d’analyse du catalogue se produit.

>[!NOTE]
>
>Les caractères suivants sont utilisés comme délimiteurs d’ensemble et doivent être codés en HTTP lorsqu’ils apparaissent dans l’ensemble en tant que partie de valeurs id ou string :
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


Reportez-vous à la documentation Image Serving Viewers pour plus de détails sur la structure et l’utilisation des visionneuses d’images.

Le serveur renvoie le contenu de ce champ sans modification en réponse à une `req=imageset` requête.

## Ensembles standard {#section-5ecc8ffee7224668b63f601383665564}

Les définitions de jeu suivantes sont prises en charge en mode natif par Image Server, et l’accès avec certaines visionneuses implique l’analyse, la validation et le traitement de la visionneuse côté serveur. Chaque type d’ensemble peut être identifié en spécifiant la valeur correspondante dans `catalog::AssetType`.

**Séries d’échantillons de base**

Chaque élément d’une série d’échantillons de base se compose d’une référence à un enregistrement d’image et d’une référence distincte facultative à un enregistrement d’image utilisé comme échantillon.

| `*`Série d’échantillons de base`*` | `*`Élément`*&#42;[',' *`d’échantillon Élément d’échantillon`*]` |
|---|---|
| `*`Élément d’échantillon`*` | `*`Échantillon d’ID d’image`*[';' *` `*]` |
| `*`échantillon`*` | `*`Identifiant de l’échantillon`*|solidColorSpecifier` |
| `*`ID d’image`*` | Référence d’image IS (catalogue/id) |
| `*`Identifiant de l’échantillon`*` | Référence d’image IS (catalogue/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *`étiquette rrggbb`* [ *` `*]'}'` |
| `*`rrggbb`*` | Valeur de couleur RVB hexadécimale à 6 chiffres emballée pour les échantillons de couleur unie |
| `*`étiquette`*` | Libellé de texte facultatif pour les échantillons de couleur unie |

**Série d’échantillons hiérarchiques**

Chaque élément d’une série d’échantillons hiérarchiques peut consister en un élément d’échantillon de base ou une référence à un enregistrement de série d’échantillons (des échantillons sont requis pour ces articles).

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`Élément d’échantillon`* | { *`de baseSwatchSetId`* ';' *`Nuance`* }` |
| `*`Identifiant de base`*` | Référence IS (catalogue/id) à un enregistrement de catalogue définissant une série d’échantillons de base |

**Visionneuses à 360° de base**

Une visionneuse à 360° de base consiste en une simple liste d’ID d’image.

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**Visionneuses à 360° bidimensionnelles**

Chaque élément d’une visionneuse à 360° bidimensionnelle peut consister en une image simple, une référence à une visionneuse à 360° de base ou une visionneuse à 360° de base en ligne délimitée par des accolades. Des parenthèses peuvent être utilisées à la place d’accolades.

| `*`2dÉlément de rotation`*` | `*`2dVisionneuse`* *`à 360° 2dÉlément`* &#42;[ ',' *`de rotation 2dÉlément de rotation`* ]` |
|---|---|
| `*`2dÉlément de rotation`*` | `*`ID d’image`* | { '{' *`Visionneuse à 360`* '}' } | *`° de base`*` |
| `*`Identifiant du jeu de rotations de base`*` | Référence IS (catalogue/id) à un enregistrement de catalogue définissant une visionneuse à 360° de base |

**Jeux de pages**

Chaque élément d’un jeu de pages peut contenir jusqu’à trois images séparées par deux points.

| `*`Visionneuse de pages`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`Élément de page`*` | `*`ID d’image`* [ : *`ID d’image`* [ : *`ID d’image`* ] ]` |

**Visionneuses de supports**

Chaque élément d’une visionneuse de supports peut se composer d’une image, d’une série d’échantillons de base, d’une série d’échantillons hiérarchiques, d’une visionneuse à 360° de base, d’une visionneuse à 360° bidimensionnelle, d’une visionneuse de pages ou d’une ressource vidéo. Chaque élément de visionneuse de supports peut également contenir un identifiant de type et d’échantillon facultatif.

| `*`Visionneuse de supports`*` | `*`élément`* &#42;[ , *` `* ]` |
|---|---|
| `*`article`*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`reserved`* ] ] ]` |
| `*`Élément vidéo`*` | `*`Identifiant de l’échantillon vidéo`* ; *` `*` |
| `*`RecutItem`*` | `*`Recut`* ; *`swatchId`*` |
| `*`Élément d’image`*` | `*`ID d’image`* ; [ *`Identifiant de la nuance`* ]` |
| `*`Élément défini`*` | ` { *`setId`* | { '{' *`Jeu intégré`* '}' } } ; *`Identifiant de la nuance swatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`Identifiant de l’échantillon`*` | ID d’image IS |
| `*`vidéo`*` | Chemin de fichier vidéo/animation ou ID de catalogue statique |
| `*`Recut`*` | Chemin de fichier XML de définition de découpe ou identifiant de catalogue statique |
| `*`ID d’image`*` | ID d’image IS |
| `*`setId`*` | Référence IS à la visionneuse d’images, à 360° ou de catalogue électronique |
| `*`Ensemble en ligne`*` | Visionneuse d’images intégrées, à 360° ou de catalogue électronique |
| `*`réservé`*` | Réservé en vue d’une utilisation ultérieure |

**Visionneuses de vidéos**

Une visionneuse de vidéos se compose d’une simple liste d’ID vidéo où chaque ID fait référence à une entrée du catalogue de contenu statique.

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## Propriétés {#section-17c731e5c46646aa90ac21f39bb693ca}

Chaîne de texte. liste de valeurs séparées par des virgules, chemins absolus aux `catalog::Id` fichiers Image Server ou chemins d’accès aux fichiers relatifs à `attribute::RootPath`. Une même image peut être référencée plusieurs fois dans l’ensemble. L’enregistrement de catalogue de définition peut apparaître dans l’ensemble à n’importe quel emplacement.

Ce champ participe à la localisation des chaînes de texte. *`label`* Outre les chaînes (qui font partie du ) tous les champs délimités sont localisés s’ils incluent au moins un jeton de *`solidColorSpecifier`* localisation &#39; `^loc=…^`&#39;. Pour plus d’informations, reportez-vous à [la section Localisation](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) de chaînes de texte dans la section Référence *du* protocole HTTP.

## Par défaut {#section-c3a60e360393478284f0f2d2da5b963b}

Aucune

## Voir également {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute ::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Traduction](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) d’ID d’objet , [Localisation de](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) chaîne de texte , Documentation du serveur d’images
