---
description: Incorporer XMP métadonnées. Indique si XMP métadonnées doivent être incluses dans l’image de réponse.
seo-description: Incorporer XMP métadonnées. Indique si XMP métadonnées doivent être incluses dans l’image de réponse.
seo-title: xmpEmbed
solution: Experience Manager
title: xmpEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: c0dfd0e5-16d1-4a6e-957a-ecc276b9361a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---


# xmpEmbed{#xmpembed}

Incorporer XMP métadonnées. Indique si XMP métadonnées doivent être incluses dans l’image de réponse.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP données sont transmises de l’image source à l’image de réponse sans modification. Cela peut entraîner l’incorporation de données incorrectes dans l’image de réponse.

## Propriétés {#section-27024c4272f44d9a8c264a0629193af2}

Attribut de requête. Ignoré si l’image source ne contient pas de données XMP. Seules les données XMP de l&#39;image source de `layer=0` sont traitées. XMP données provenant d’autres images de calque sont ignorées.

Ignoré si le format d’image de sortie ne prend pas en charge XMP incorporation. Reportez-vous à la description de `fmt=` pour obtenir une liste des formats d’image de sortie qui prennent en charge l’incorporation XMP.

## Par défaut {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, pour ne pas incorporer de chemins dans les images de sortie.

## Voir aussi {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
