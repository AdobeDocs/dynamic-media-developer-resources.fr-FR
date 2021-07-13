---
description: Incorporer XMP métadonnées. Indique si XMP métadonnées doivent être incluses dans l’image de réponse.
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# xmpEmbed{#xmpembed}

Incorporer XMP métadonnées. Indique si XMP métadonnées doivent être incluses dans l’image de réponse.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP données sont transmises de l’image source à l’image de réponse sans modification. Cela peut entraîner l’incorporation de données incorrectes dans l’image de réponse.

## Propriétés {#section-27024c4272f44d9a8c264a0629193af2}

Attribut de requête. Ignoré si l’image source ne contient pas XMP données. Seules les données XMP de l’image source de `layer=0` sont traitées. Les données XMP d’autres images de calque sont ignorées.

Ignoré si le format d’image de sortie ne prend pas en charge XMP incorporation. Reportez-vous à la description de `fmt=` pour obtenir la liste des formats d’image de sortie qui prennent en charge XMP’incorporation.

## Par défaut {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, sans incorporation de chemins dans les images de sortie.

## Voir aussi {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
