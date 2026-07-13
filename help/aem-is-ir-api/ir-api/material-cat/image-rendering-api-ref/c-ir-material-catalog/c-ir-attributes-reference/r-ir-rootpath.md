---
title: RootPath
description: Chemin d’accès racine des données Source. Valeur de chaîne de texte. Chemin d’accès absolu ou segment de chemin d’accès relatif pour le dossier racine de tous les fichiers de données de vignette, de texture, d’image et ICC référencés par ce catalogue d’images.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
TQID: 'https://experienceleague.adobe.com/yCtXjcZDG0HCqydirr7TDe5-e0oWtHmlvAxHDl-gfac'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 2%

---

# RootPath{#rootpath}

Chemin d’accès racine des données Source. Valeur de chaîne de texte. Chemin d’accès absolu ou segment de chemin d’accès relatif pour le dossier racine de tous les fichiers de données de vignette, de texture, d’image et ICC référencés par ce catalogue d’images.

## Propriétés {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Chaîne de texte. Doit être vide, un segment de chemin valide relatif au paramètre de configuration du serveur de rendu d’images `ir.resourceRootPaths`, ou un chemin d’accès au fichier absolu valide. Ne doit pas inclure de délimiteurs d’élément de chemin de début et de fin.

## Par défaut {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Hérité de `default::RootPath` si non défini. S’il est défini mais vide, il ne contribue pas au chemin d’accès racine du fichier source.

## Voir aussi {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) , [catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969), `ir.resourceRootPaths`

