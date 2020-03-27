---
description: Informations utilisateur Digimarc. Spécifie les informations utilisateur pour l’incorporation de Digimarc.
seo-description: Informations utilisateur Digimarc. Spécifie les informations utilisateur pour l’incorporation de Digimarc.
seo-title: DigimarcId
solution: Experience Manager
title: DigimarcId
topic: Scene7 Image Serving - Image Rendering API
uuid: 23f1952f-71b7-4b2a-917d-8161ea855ac9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DigimarcId{#digimarcid}

Informations utilisateur Digimarc. Spécifie les informations utilisateur pour l’incorporation de Digimarc.

## Propriétés {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Cinq ou six nombres entiers séparés par des virgules. Les troisième et quatrième numéros ne sont plus utilisés :

`creator-id, creator-pin, durability [ , chroma ]`

Les `creator-id` et `creator-pin` sont fournis par Digimarc lors de l&#39;achat du service. Les valeurs inutilisées doivent rester vides.

`durability` spécifie la résistance d’incorporation du filigrane Digimarc. Il peut s’agir de 1, 2, 3 ou 4, 1 indiquant la durabilité la plus faible et 4 la plus robuste.

Définissez `chroma` sur 1 pour coder le filigrane dans les données de chrominance de l’image ou sur 0 (valeur par défaut) pour le coder dans la luminance. Ce paramètre est ignoré lors de la sortie d’images en niveaux de gris.

## Par défaut {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Héritée de `default::DigimarcId` si non définie ou si vide.

## Exemple {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Spécifiez un ID de créateur Digimarc de test dont la durabilité est définie sur 4.

`DigimarcId= 404407,32,,,4`

## Voir aussi {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalogue ::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
