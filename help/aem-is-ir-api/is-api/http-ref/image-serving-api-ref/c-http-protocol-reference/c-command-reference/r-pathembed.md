---
title: pathEmbed
description: Incorporer les données de chemins d’accès. Indique si les chemins Photoshop du fichier image source de la couche 0 doivent être inclus dans l’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
TQID: 'https://experienceleague.adobe.com/ES7nAoYjO6Y4naU2c5TIPotPUTjncwjRMLL7-4--XpE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 2%

---

# pathEmbed{#pathembed}

Incorporer les données de chemins d’accès. Indique si les chemins Photoshop du fichier image source de la couche 0 doivent être inclus dans l’image de réponse.

`pathEmbed=0|1`

## Propriétés {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Attribut de requête. Ignoré si l’image source ne contient pas de données de chemins. Les données de chemins sont mises à l’échelle et pivotées comme les données d’image. Seuls les chemins d’accès provenant de l’image source de `layer=0` sont traités. Les chemins d’accès provenant d’autres images de calque sont ignorés.

Ignoré si le format d’image de sortie ne prend pas en charge l’incorporation de chemin. Reportez-vous à la description de `fmt=` pour obtenir une liste des formats d’image de sortie qui prennent en charge l’incorporation de chemins d’accès.

## Restrictions {#section-697cddb79a1542bc8457d2f4f59eec69}

Les chemins d’accès Photoshop ouverts (qui ne forment pas de boucles fermées) ne sont pas pris en charge pour l’incorporation dans l’image de réponse pour le moment.

## Par défaut {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, pour l’absence d’incorporation de chemins dans les images de sortie.

## Voir aussi {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
