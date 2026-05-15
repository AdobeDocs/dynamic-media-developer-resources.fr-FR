---
description: Informations sur l'utilisateur Digimarc. Spécifie les informations utilisateur pour l'incorporation Digimarc.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
TQID: 'https://experienceleague.adobe.com/2kkvN1RLEhbDEmN4cA6lE5nGe9d-T3qcdxgGqF7L3Ig'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 2%

---

# DigimarcId{#digimarcid}

Informations sur l&#39;utilisateur Digimarc. Spécifie les informations utilisateur pour l&#39;incorporation Digimarc.

## Propriétés {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Cinq ou six nombres entiers séparés par des virgules. Les troisième et quatrième numéros ne sont plus utilisés :

`creator-id, creator-pin, durability [ , chroma ]`

Les `creator-id` et `creator-pin` sont fournis par Digimarc lors de l&#39;achat du service. Les valeurs inutilisées doivent rester vides.

`durability` spécifie la résistance d&#39;incorporation du filigrane Digimarc. Il peut s’agir de 1, 2, 3 ou 4, 1 indiquant la durabilité la plus faible et 4 la plus forte.

Définissez `chroma` sur 1 pour coder le filigrane dans les données de chrominance de l’image ou sur 0 (par défaut) pour le coder dans la luminance. Ce paramètre est ignoré lors de la sortie d’images en niveaux de gris.

## Par défaut {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Hérité de `default::DigimarcId` si non défini ou si vide.

## Exemple {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Spécifiez un identifiant de créateur Digimarc de test dont la durabilité est définie sur 4.

`DigimarcId= 404407,32,,,4`

## Voir aussi {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
