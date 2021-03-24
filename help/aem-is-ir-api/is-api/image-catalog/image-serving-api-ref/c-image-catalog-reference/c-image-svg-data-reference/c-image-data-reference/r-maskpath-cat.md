---
description: Chemin du fichier de masquage. Chemin d’accès relatif ou absolu et nom d’un fichier image de masque associé à cet enregistrement de catalogue.
solution: Experience Manager
title: MasquePath
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---


# MaskPath{#maskpath}

Chemin du fichier de masquage. Chemin d’accès relatif ou absolu et nom d’un fichier image de masque associé à cet enregistrement de catalogue.

Permet d’associer des masques distincts à des images.

Le serveur utilise les règles de résolution de chemin décrites dans [Gestion des données source](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) pour trouver le fichier de données.

## Propriétés {#section-cdc3b7e2811e41008479cd97887c01b7}

Valeur de chaîne de texte. Facultatif. S’il est spécifié, il doit s’agir d’un chemin d’accès au fichier Image Server relatif ou absolu valide. `attribute::DefaultExt` est ajouté si aucun suffixe de fichier n’est présent.

Si une image principale ( `catalog::Path`) et une image de masque ( `catalog::MaskPath`) sont définies toutes deux dans un enregistrement de catalogue, elles doivent avoir exactement la même taille de pixel. Les images de masquage doivent être en niveaux de gris 8 bits.

`mask=` dans la requête remplace  `catalog::MaskPath`.

`catalog::MaskPath` remplace le canal alpha dans l’image principale (  `catalog::Path`), le cas échéant, et si le canal alpha n’est pas associé (c’est-à-dire qu’il n’est pas prémultiplié). Si l’image alpha est prémultipliée, `catalog::MaskPath` est ignoré et le canal alpha est toujours utilisé.

## Par défaut {#section-78533e35bfec469ba087cb68a35bb81b}

Aucune

## Voir aussi {#section-68d262f5949c4959b8723ba44611d1dc}

[attribut::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [attribut::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md),  [catalogue::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c),  [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)[
