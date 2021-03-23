---
description: Incorporer les données de chemins. Indique si les chemins Photoshop du fichier image source du calque 0 doivent être inclus dans l’image de réponse.
seo-description: Incorporer les données de chemins. Indique si les chemins Photoshop du fichier image source du calque 0 doivent être inclus dans l’image de réponse.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
uuid: 93e63c7c-c091-4bb1-baff-45706fd611ea
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---


# pathEmbed{#pathembed}

Incorporer les données de chemins. Indique si les chemins Photoshop du fichier image source du calque 0 doivent être inclus dans l’image de réponse.

`pathEmbed=0|1`

## Propriétés {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Attribut de requête. Ignoré si l’image source ne contient pas de données de chemins d’accès. Les données de chemins sont mises à l’échelle et pivotées comme les données d’image. Seuls les chemins d’accès à partir de l’image source de `layer=0` sont traités ; les chemins d’accès d’autres images de calque sont ignorés.

Ignoré si le format d’image de sortie ne prend pas en charge l’incorporation de chemins. Reportez-vous à la description de `fmt=` pour obtenir une liste des formats d’image de sortie qui prennent en charge l’incorporation de chemins.

## Restrictions {#section-697cddb79a1542bc8457d2f4f59eec69}

Pour le moment, les chemins Photoshop ouverts (chemins qui ne forment pas de boucles fermées) ne sont pas pris en charge pour l’incorporation dans l’image de réponse.

## Par défaut {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, pour ne pas incorporer de chemins dans les images de sortie.

## Voir aussi {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
