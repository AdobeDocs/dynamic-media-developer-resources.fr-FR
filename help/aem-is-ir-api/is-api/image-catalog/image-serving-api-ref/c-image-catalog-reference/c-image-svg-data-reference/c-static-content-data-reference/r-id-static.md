---
description: ID
solution: Experience Manager
title: ID
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 5%

---

# ID{#id}

En règle générale, il s’agit d’un identifiant court et unique, tel qu’un numéro de SKU, éventuellement doté d’un suffixe, comme si un SKU comporte plusieurs images ou comporte des variantes propres aux paramètres régionaux. Il peut également s’agir d’une chaîne plus complexe, qui ressemble davantage à un chemin d’accès au fichier, afin de faciliter la mise à niveau des sites web avec le serveur d’images.

>[!NOTE]
>
>Les tables image et SVG sont fusionnées en une seule table lors du chargement du catalogue d’images. Les valeurs d’identifiant doivent être uniques dans les deux tableaux. L’enregistrement SVG est ignoré si la table des images contient un enregistrement avec la même valeur d’identifiant. Le contenu statique est géré avec une table distincte ; les éléments de contenu statique et les éléments image/SVG peuvent donc avoir les mêmes valeurs d’identifiant.

## Propriétés {#section-874a6853f67b4b229341ca76682884ae}

Chaîne de texte. Obligatoire. Identifiant d’enregistrement de la table de données image/SVG ou de contenu statique. Chaque valeur `catalog::Id` dans ce catalogue d’images/SVG ou dans ce catalogue de contenu statique doit être unique et ne doit pas contenir de caractères &quot;,&quot;.

## Par défaut {#section-a26e7d83a5ee44b5918baef82ee48e14}

Aucune

## Voir aussi {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
