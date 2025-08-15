---
description: Informations sur l’utilisateur Digimarc. Spécifie les informations de l’utilisateur pour l’incorporation de Digimarc.
solution: Experience Manager
title: ID digimicaux
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# ID digimicaux{#digimarcid}

Informations sur l’utilisateur Digimarc. Spécifie les informations de l’utilisateur pour l’incorporation de Digimarc.

## Propriétés {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Cinq ou six nombres entiers séparés par des virgules. Les troisième et quatrième numéros ne sont plus utilisés :

`creator-id, creator-pin, durability [ , chroma ]`

Les `creator-id` et `creator-pin` sont fournis par Digimarc lors de l’achat du service. Les valeurs inutilisées doivent être vides.

`durability` spécifie la force d’incorporation du filigrane Digimarc. Il peut s’agir de 1, 2, 3 ou 4, 1 indiquant la durabilité la plus faible et 4 la plus forte.

Définissez `chroma` ce paramètre sur 1 pour coder le filigrane dans les données de chrominance de l’image ou sur 0 (par défaut) pour le coder dans la luminance. Ce paramètre est ignoré lors de la sortie des images en niveaux de gris.

## Par défaut {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Hérité de `default::DigimarcId` si non défini ou si vide.

## Exemple {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Spécifiez un identifiant de créateur Digimarc de test avec une durabilité définie sur 4.

`DigimarcId= 404407,32,,,4`

## Voir aussi {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalogue ::D igimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
