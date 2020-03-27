---
description: 'null'
seo-description: 'null'
seo-title: ID
solution: Experience Manager
title: ID
topic: Scene7 Image Serving - Image Rendering API
uuid: 45a79636-3fa9-4f2a-98bb-a46c9b627dd4
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# ID{#id}

En règle générale, un identifiant court et unique, tel qu’un numéro SKU, peut être doté d’un suffixe, comme si un SKU comporte plusieurs images ou des variations propres aux paramètres régionaux. Il peut également s’agir d’une chaîne plus complexe qui ressemble davantage à un chemin de fichier, afin de faciliter la modification des sites Web avec la diffusion d’images.

>[!NOTE]
>
>Les tableaux image et SVG sont fusionnés dans un seul tableau lorsque le catalogue d’images est chargé. Les valeurs d’ID doivent être uniques dans les deux tableaux. L’enregistrement SVG est ignoré si la table d’images contient un enregistrement avec la même valeur d’ID. Le contenu statique est géré avec un tableau distinct ; les éléments de contenu statique et les éléments image/SVG peuvent donc avoir les mêmes valeurs d’ID.

## Propriétés {#section-874a6853f67b4b229341ca76682884ae}

Chaîne de texte. Obligatoire. Identifiant d’enregistrement pour l’image/le SVG ou le tableau de données de contenu statique. Chaque `catalog::Id` valeur de ce catalogue d’images/catalogue SVG ou de ce catalogue de contenu statique doit être unique et ne doit pas inclure de caractères &quot;,&quot;.

## Par défaut {#section-a26e7d83a5ee44b5918baef82ee48e14}

Aucune

## Voir aussi {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
