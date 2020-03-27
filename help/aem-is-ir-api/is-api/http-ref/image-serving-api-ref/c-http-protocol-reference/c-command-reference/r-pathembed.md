---
description: Incorporer les données de chemins. Indique si les chemins d’accès Photoshop du fichier image source du calque 0 doivent être inclus dans l’image de réponse.
seo-description: Incorporer les données de chemins. Indique si les chemins d’accès Photoshop du fichier image source du calque 0 doivent être inclus dans l’image de réponse.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: 93e63c7c-c091-4bb1-baff-45706fd611ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pathEmbed{#pathembed}

Incorporer les données de chemins. Indique si les chemins d’accès Photoshop du fichier image source du calque 0 doivent être inclus dans l’image de réponse.

`pathEmbed=0|1`

## Propriétés {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Attribut de requête. Ignoré si l’image source ne contient pas de données de chemins d’accès. Les données des chemins sont mises à l’échelle et pivotées comme les données d’image. Seuls les chemins de l’image source de `layer=0` sont traités ; les chemins d’autres images de calque sont ignorés.

Ignoré si le format d’image de sortie ne prend pas en charge l’incorporation de chemins. Reportez-vous à la description de `fmt=` pour un de formats d’image de sortie prenant en charge l’incorporation de chemins.

## Restrictions {#section-697cddb79a1542bc8457d2f4f59eec69}

Les chemins d’accès Photoshop ouverts (chemins qui ne forment pas de boucles fermées) ne sont pas pris en charge pour l’instant pour l’incorporation dans l’image de réponse.

## Par défaut {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, pour ne pas incorporer de chemins dans les images de sortie.

## Voir aussi {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
