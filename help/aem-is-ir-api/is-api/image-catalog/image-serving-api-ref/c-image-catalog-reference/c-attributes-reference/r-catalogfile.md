---
description: Chemins d’accès aux fichiers de données image. Spécifie les fichiers qui contiennent les données image pour ce catalogue.
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
TQID: 'https://experienceleague.adobe.com/MhxEBtyw3JIvMg5miQotPPCeoLeWATtXy0fbRtE7ePs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 3%

---

# CatalogFile{#catalogfile}

Chemins d’accès aux fichiers de données image. Spécifie les fichiers qui contiennent les données image pour ce catalogue.

Les fichiers de données d’image sont chargés dans l’ordre spécifié. Si la même valeur de `catalog::Id` apparaît dans plusieurs enregistrements (dans le même fichier catalogue ou dans des fichiers catalogues différents), la dernière instance prévaut.

## Propriétés {#section-6da55f145ecd4e31a5de52637a436983}

Une ou plusieurs valeurs de chaîne de texte, séparées par des virgules. Facultatif. Chaque valeur doit être un chemin d’accès absolu au fichier ou un chemin d’accès relatif au dossier du catalogue.

## Par défaut {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vide, ce qui indique que ce catalogue d’images n’inclut aucune donnée d’image.

## Voir aussi {#section-910b67c5041d44d99a105ad43ff63a37}

[Champs de données de catalogue](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
