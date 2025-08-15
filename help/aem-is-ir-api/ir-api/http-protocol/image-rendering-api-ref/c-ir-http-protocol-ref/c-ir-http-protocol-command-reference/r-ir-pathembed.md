---
title: pathEmbed
description: Incorporer les données de chemins d’accès. Indique si les chemins Photoshop incorporés dans la vignette doivent être inclus dans l’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# pathEmbed{#pathembed}

Incorporer les données de chemins d’accès. Indique si les chemins Photoshop incorporés dans la vignette doivent être inclus dans l’image de réponse.

`pathEmbed=0|1`

## Propriétés {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Attribut de requête. Ignoré si la vignette ne contient pas de données de chemins. Les données de chemins sont mises à l’échelle sur `wid=` et/ou `hei=` si nécessaire.

Ignoré si le format d’image de sortie ne prend pas en charge l’incorporation de chemin. Reportez-vous à la description de `fmt=` pour obtenir une liste des formats d’image de sortie qui prennent en charge l’incorporation de chemins d’accès.

## Par défaut {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, pour l’absence d’incorporation de chemins dans les images de sortie.

## Voir aussi {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
