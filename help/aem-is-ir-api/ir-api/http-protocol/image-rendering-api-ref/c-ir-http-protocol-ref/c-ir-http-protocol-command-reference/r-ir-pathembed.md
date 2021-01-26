---
description: Incorporer les données de chemins. Indique si les chemins Photoshop incorporés dans la vignette doivent être inclus dans l’image de réponse.
seo-description: Incorporer les données de chemins. Indique si les chemins Photoshop incorporés dans la vignette doivent être inclus dans l’image de réponse.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d40ea1b5-f2d3-4f81-b96f-abb4eb7eb2b3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 3%

---


# pathEmbed{#pathembed}

Incorporer les données de chemins. Indique si les chemins Photoshop incorporés dans la vignette doivent être inclus dans l’image de réponse.

`pathEmbed=0|1`

## Propriétés {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Attribut de requête. Ignoré si la vignette ne contient pas de données de chemins d’accès. Si nécessaire, les données des chemins sont mises à l’échelle `wid=` et/ou `hei=`.

Ignoré si le format d’image de sortie ne prend pas en charge l’incorporation de chemins. Reportez-vous à la description de `fmt=` pour obtenir une liste des formats d’image de sortie qui prennent en charge l’incorporation de chemins.

## Par défaut {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, pour ne pas incorporer de chemins dans les images de sortie.

## Voir aussi {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
