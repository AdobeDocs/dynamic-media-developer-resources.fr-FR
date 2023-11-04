---
description: Masquer le chemin d’accès au fichier. Chemin d’accès relatif ou absolu et nom d’un fichier image de masque associé à cet enregistrement de catalogue.
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# MaskPath{#maskpath}

Masquer le chemin d’accès au fichier. Chemin d’accès relatif ou absolu et nom d’un fichier image de masque associé à cet enregistrement de catalogue.

Permet d’associer des masques distincts aux images.

Le serveur utilise les règles de résolution de chemin décrites dans la section [Gestion des données source](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) pour rechercher le fichier de données.

## Propriétés {#section-cdc3b7e2811e41008479cd97887c01b7}

Valeur de chaîne de texte. Facultatif. S’il est spécifié, il doit s’agir d’un chemin d’accès au fichier Image Server relatif ou absolu valide. `attribute::DefaultExt` est ajouté si aucun suffixe de fichier n’est présent.

Si les deux images principales ( `catalog::Path`) et une image de masque ( `catalog::MaskPath`) sont définis dans un enregistrement de catalogue, les deux doivent avoir exactement la même taille de pixel. Les images de masque doivent être en niveaux de gris 8 bits.

`mask=` dans les remplacements de requête `catalog::MaskPath`.

`catalog::MaskPath` remplace le canal alpha dans l’image principale ( `catalog::Path`), le cas échéant, et si le canal alpha n’est pas associé (c’est-à-dire qu’il n’est pas pré-multiplié). Si l&#39;image alpha est pré-multipliée, `catalog::MaskPath` est ignorée et le canal alpha est toujours utilisé.

## Par défaut {#section-78533e35bfec469ba087cb68a35bb81b}

Aucune

## Voir aussi {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
