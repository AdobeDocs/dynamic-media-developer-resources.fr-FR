---
description: Chemin du fichier des mesures de police. Chemin d’accès et nom d’un fichier de mesures de polices, y compris le suffixe du fichier.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---


# MetricsPath{#metricspath}

Chemin du fichier des mesures de police. Chemin d’accès et nom d’un fichier de mesures de polices, y compris le suffixe du fichier.

Utilisé pour les polices Adobe Type 1. Si elle n’est pas spécifiée, le serveur tente de trouver un fichier de mesures de polices dans le dossier où se trouve le fichier de polices principal. Une erreur se produit si un fichier de mesures de police requis est introuvable au moment du rendu.

## Propriétés {#section-955268c581574875b05253d9e14544f3}

Chaîne de texte. Facultatif pour les fichiers Adobe Type 1. Doit être vide ou un chemin d’accès au fichier Image Server valide, absolu ou relatif à `attribute::RootPath`.

## Par défaut {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Aucune

## Voir aussi {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribut::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
