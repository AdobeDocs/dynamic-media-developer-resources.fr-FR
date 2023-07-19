---
title: ID
description: En règle générale, un identifiant court et unique, tel qu’un numéro de SKU, peut-être doté d’un suffixe, par exemple si un SKU comporte plusieurs images ou comporte des variantes propres aux paramètres régionaux.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d7b37180-cc93-41cd-bf14-5c262b046fbc
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# ID{#id}

En règle générale, un identifiant court et unique, tel qu’un numéro de SKU, peut-être doté d’un suffixe, par exemple si un SKU comporte plusieurs images ou comporte des variantes propres aux paramètres régionaux. Il peut également s’agir d’une chaîne plus complexe, qui ressemble davantage à un chemin d’accès au fichier, afin de faciliter la mise à niveau des sites web avec le serveur d’images.

>[!NOTE]
>
>Les tableaux d’image et de SVG sont fusionnés en une seule table lors du chargement du catalogue d’images. Les valeurs d’identifiant doivent être uniques dans les deux tableaux. L’enregistrement du SVG est ignoré si la table des images contient un enregistrement avec la même valeur d’identifiant. Le contenu statique est géré avec une table distincte ; les éléments de contenu statique et les éléments image/SVG peuvent donc avoir les mêmes valeurs d’identifiant.

## Propriétés {#section-874a6853f67b4b229341ca76682884ae}

Chaîne de texte. Obligatoire. Identifiant d’enregistrement de la table de données image/SVG ou de contenu statique. Chaque `catalog::Id` dans ce catalogue d’images/de SVG ou dans ce catalogue de contenu statique doit être unique et ne doit pas contenir de caractères &quot;,&quot;.

## Par défaut {#section-a26e7d83a5ee44b5918baef82ee48e14}

Aucune

## Voir aussi {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
