---
description: Chemin du fichier Vignette. Chemin relatif et nom d’un fichier de vignette.
solution: Experience Manager
title: Chemin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5562b0e0-0476-4dd0-acce-058601b9af0a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 8%

---

# Chemin{#path}

Chemin du fichier Vignette. Chemin relatif et nom d’un fichier de vignette.

Le serveur combine cette valeur avec `attribute::RootPath` pour créer le chemin d’accès réel au fichier de vignette. Peut également être un chemin absolu.

## Propriétés {#section-b3b295feac084b56bd8a153c04987153}

Chaîne de texte. Facultatif. S’il est spécifié, il doit s’agir d’un chemin d’accès relatif ou absolu valide. Si vide, `vignette::Modifier` devez inclure la commande `vignette=`.

## Par défaut {#section-a1d2133856084eb79a5be8230a4b38fd}

Aucune

## Voir aussi {#section-177131dad5804964bfb8957c1f6e5191}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
