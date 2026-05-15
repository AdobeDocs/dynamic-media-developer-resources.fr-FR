---
description: Masquez le chemin d’accès au fichier. Chemin d’accès et nom relatifs ou absolus d’un fichier image de masque associé à cet enregistrement de catalogue.
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
TQID: 'https://experienceleague.adobe.com/tUXD-vnkr3qkaH3B-dE-e9wfSPXAcnwRbqG9KuJej9E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 2%

---

# MaskPath{#maskpath}

Masquez le chemin d’accès au fichier. Chemin d’accès et nom relatifs ou absolus d’un fichier image de masque associé à cet enregistrement de catalogue.

Permet de joindre des masques distincts aux images.

Le serveur utilise les règles de résolution de chemin d’accès décrites dans la section [Gestion des données Source](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) pour rechercher le fichier de données.

## Propriétés {#section-cdc3b7e2811e41008479cd97887c01b7}

Valeur de chaîne de texte. Facultatif. S’il est spécifié, il doit s’agir d’un chemin d’accès relatif ou absolu au fichier Image Server valide. `attribute::DefaultExt` est ajouté si aucun suffixe de fichier n’est présent.

Si une image principale (`catalog::Path`) et une image de masque (`catalog::MaskPath`) sont définies dans un enregistrement de catalogue, les deux doivent avoir exactement la même taille en pixels. Les images de masque doivent être en niveaux de gris 8 bits.

`mask=` dans la requête remplace `catalog::MaskPath`.

`catalog::MaskPath` remplace la couche alpha dans l’image principale ( `catalog::Path`), le cas échéant, et si la couche alpha n’est pas associée (c’est-à-dire qu’elle n’est pas prémultipliée). Si la couche alpha de l’image est pré-multipliée, `catalog::MaskPath` est ignorée et la couche alpha est toujours utilisée.

## Par défaut {#section-78533e35bfec469ba087cb68a35bb81b}

Aucune

## Voir aussi {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
