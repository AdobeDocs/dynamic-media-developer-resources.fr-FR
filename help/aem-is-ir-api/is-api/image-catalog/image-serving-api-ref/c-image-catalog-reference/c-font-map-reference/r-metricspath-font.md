---
description: Chemin d’accès au fichier des mesures de police. Chemin et nom d’un fichier de mesures de polices, y compris le suffixe du fichier.
seo-description: Chemin d’accès au fichier des mesures de police. Chemin et nom d’un fichier de mesures de polices, y compris le suffixe du fichier.
seo-title: MetricsPath
solution: Experience Manager
title: MetricsPath
topic: Scene7 Image Serving - Image Rendering API
uuid: b59110bf-330f-4ca4-8b0a-219a61d383f7
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# MetricsPath{#metricspath}

Chemin d’accès au fichier des mesures de police. Chemin et nom d’un fichier de mesures de polices, y compris le suffixe du fichier.

Utilisé pour les polices Adobe Type 1. S’il n’est pas spécifié, le serveur tente de trouver un fichier de mesures de polices dans le dossier où se trouve le fichier de polices principal. Une erreur se produira si un fichier de mesures de polices requis est introuvable au moment du rendu.

## Propriétés {#section-955268c581574875b05253d9e14544f3}

Chaîne de texte. Facultatif pour les fichiers Adobe Type 1. Doit être vide ou un chemin d’accès au fichier Image Server valide, absolu ou relatif à `attribute::RootPath`.

## Par défaut {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Aucune

## Voir aussi {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribut:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
