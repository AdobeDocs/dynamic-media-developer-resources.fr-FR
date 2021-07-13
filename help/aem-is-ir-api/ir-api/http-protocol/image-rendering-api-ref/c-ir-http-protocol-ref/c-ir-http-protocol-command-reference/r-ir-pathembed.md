---
description: Incorporer les données de chemins d’accès. Indique si les chemins Photoshop incorporés dans la vignette doivent être inclus dans l’image de réponse.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# pathEmbed{#pathembed}

Incorporer les données de chemins d’accès. Indique si les chemins Photoshop incorporés dans la vignette doivent être inclus dans l’image de réponse.

`pathEmbed=0|1`

## Propriétés {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Attribut de requête. Ignoré si la vignette ne contient pas de données de chemins. Si nécessaire, les données de chemins sont mises à l’échelle vers `wid=` et/ou `hei=`.

Ignoré si le format d’image de sortie ne prend pas en charge l’incorporation des chemins. Reportez-vous à la description de `fmt=` pour obtenir la liste des formats d’image de sortie qui prennent en charge l’incorporation des chemins.

## Par défaut {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, sans incorporation de chemins dans les images de sortie.

## Voir aussi {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
