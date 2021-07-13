---
description: Chemin d’accès au fichier des mesures de police. Chemin et nom d’un fichier de mesures de police, y compris le suffixe de fichier.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# MetricsPath{#metricspath}

Chemin d’accès au fichier des mesures de police. Chemin et nom d’un fichier de mesures de police, y compris le suffixe de fichier.

Utilisé pour les polices Adobe Type 1. S’il n’est pas spécifié, le serveur tente de trouver un fichier de mesures de police dans le dossier où se trouve le fichier de police principal. Une erreur se produit si un fichier de mesures de polices requis est introuvable au moment du rendu.

## Propriétés {#section-955268c581574875b05253d9e14544f3}

Chaîne de texte. Facultatif pour les fichiers d’Adobe Type 1. Doit être vide ou un chemin d’accès au fichier du serveur d’images valide, absolu ou relatif à `attribute::RootPath`.

## Par défaut {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Aucune

## Voir aussi {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
