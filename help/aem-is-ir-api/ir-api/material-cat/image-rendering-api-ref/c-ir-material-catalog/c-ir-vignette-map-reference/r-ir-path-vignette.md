---
description: Chemin du fichier de vignette. Chemin relatif et nom d’un fichier de vignettes.
seo-description: Chemin du fichier de vignette. Chemin relatif et nom d’un fichier de vignettes.
seo-title: Chemin
solution: Experience Manager
title: Chemin
topic: Scene7 Image Serving - Image Rendering API
uuid: 470cee37-9840-402a-bde5-ace8988996d2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 10%

---


# Chemin{#path}

Chemin du fichier de vignette. Chemin relatif et nom d’un fichier de vignettes.

Le serveur combine cette valeur avec `attribute::RootPath` pour générer le chemin d’accès réel au fichier de vignettes. Peut aussi être un chemin absolu.

## Propriétés {#section-b3b295feac084b56bd8a153c04987153}

Chaîne de texte. Facultatif. S&#39;il est spécifié, il doit s&#39;agir d&#39;un chemin d&#39;accès au fichier relatif ou absolu valide. Si la valeur est vide, `vignette::Modifier` doit inclure la commande `vignette=`.

## Par défaut {#section-a1d2133856084eb79a5be8230a4b38fd}

Aucune

## Voir aussi {#section-177131dad5804964bfb8957c1f6e5191}

[attribut::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
