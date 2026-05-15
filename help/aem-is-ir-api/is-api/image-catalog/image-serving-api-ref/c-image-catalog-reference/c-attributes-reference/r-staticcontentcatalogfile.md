---
description: Chemins d’accès statiques aux fichiers de données du catalogue de contenu. Spécifie les fichiers qui contiennent les données de contenu statique pour ce catalogue.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
TQID: 'https://experienceleague.adobe.com/98uNzMz83z3lfa2d3LNixYKZzUWWE9zqrK1fnPo-JNA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

Chemins d’accès statiques aux fichiers de données du catalogue de contenu. Spécifie les fichiers qui contiennent les données de contenu statique pour ce catalogue.

Les fichiers de données de catalogue de contenu statique sont chargés dans l’ordre spécifié. Si la même valeur de `static::Id` apparaît dans plusieurs enregistrements (dans le même fichier catalogue ou dans des fichiers catalogues différents), la dernière instance prévaut.

## Propriétés {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Une ou plusieurs valeurs de chaîne de texte, séparées par des virgules. Facultatif. Chaque valeur doit être un chemin d’accès absolu au fichier ou un chemin d’accès relatif au dossier du catalogue.

## Par défaut {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vide, ce qui indique que ce catalogue d’images n’inclut aucune donnée de contenu statique.

## Voir aussi {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Données de catalogue](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
