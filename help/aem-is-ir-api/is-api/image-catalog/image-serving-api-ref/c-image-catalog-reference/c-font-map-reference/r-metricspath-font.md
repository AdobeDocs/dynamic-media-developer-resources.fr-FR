---
description: Chemin d’accès au fichier des mesures de polices. Chemin et nom d’un fichier de mesures de polices, suffixe de fichier inclus.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
TQID: 'https://experienceleague.adobe.com/XPXcnrT94IfPupctNoxqN7-qYCuxdeoqXQeBkM1Un4k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 3%

---

# MetricsPath{#metricspath}

Chemin d’accès au fichier des mesures de polices. Chemin et nom d’un fichier de mesures de polices, suffixe de fichier inclus.

Utilisé pour les polices Adobe Type 1. S’il n’est pas spécifié, le serveur tente de trouver un fichier de mesures de police dans le même dossier que celui où se trouve le fichier de police principal. Une erreur se produit si un fichier de mesures de polices obligatoire est introuvable au moment du rendu.

## Propriétés {#section-955268c581574875b05253d9e14544f3}

Chaîne de texte. Facultatif pour les fichiers Adobe Type 1. Doit être vide ou un chemin d’accès au fichier Image Server valide, absolu ou relatif à `attribute::RootPath`.

## Par défaut {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Aucune

## Voir aussi {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
