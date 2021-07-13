---
description: Incorporer les données de chemins d’accès. Indique si les chemins Photoshop du fichier image source du calque 0 doivent être inclus dans l’image de réponse.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# pathEmbed{#pathembed}

Incorporer les données de chemins d’accès. Indique si les chemins Photoshop du fichier image source du calque 0 doivent être inclus dans l’image de réponse.

`pathEmbed=0|1`

## Propriétés {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Attribut de requête. Ignoré si l’image source ne contient pas de données de chemins d’accès. Les données de chemins sont mises à l’échelle et pivotées comme les données d’image. Seuls les chemins d’accès de l’image source de `layer=0` sont traités ; les chemins d’accès d’autres images de calque sont ignorés.

Ignoré si le format d’image de sortie ne prend pas en charge l’incorporation des chemins. Reportez-vous à la description de `fmt=` pour obtenir la liste des formats d’image de sortie qui prennent en charge l’incorporation des chemins.

## Restrictions {#section-697cddb79a1542bc8457d2f4f59eec69}

Les chemins d’accès Photoshop ouverts (chemins qui ne forment pas de boucles fermées) ne sont pas pris en charge pour l’incorporation dans l’image de réponse pour le moment.

## Par défaut {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, sans incorporation de chemins dans les images de sortie.

## Voir aussi {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
