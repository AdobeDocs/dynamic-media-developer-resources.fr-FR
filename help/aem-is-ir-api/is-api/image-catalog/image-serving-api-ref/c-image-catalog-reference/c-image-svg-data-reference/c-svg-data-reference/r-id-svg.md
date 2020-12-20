---
description: 'null'
seo-description: 'null'
seo-title: ID
solution: Experience Manager
title: ID
topic: Scene7 Image Serving - Image Rendering API
uuid: a700472c-e1eb-4eb0-95ff-7afd4ce27931
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 6%

---


# ID{#id}

En règle générale, un identifiant court et unique, tel qu’un numéro de SKU, peut-être avec un suffixe quelconque, comme si un SKU comporte plusieurs images ou a des variations spécifiques à un paramètre régional. Il peut également s’agir d’une chaîne plus complexe qui ressemble davantage à un chemin de fichier, afin de faciliter la mise à jour des sites Web avec la diffusion d’images.

>[!NOTE]
>
>Les tables image et SVG sont fusionnées en un seul tableau lorsque le catalogue d’images est chargé. Les valeurs d’ID doivent être uniques dans les deux tableaux. L’enregistrement SVG est ignoré si la table d’images contient un enregistrement avec la même valeur d’ID. Le contenu statique est géré avec un tableau distinct ; les éléments de contenu statique et les éléments image/SVG peuvent donc avoir les mêmes valeurs d’ID.

## Propriétés {#section-874a6853f67b4b229341ca76682884ae}

Chaîne de texte. Obligatoire. Identificateur d’enregistrement de l’image/du SVG ou du tableau de données de contenu statique. Chaque valeur `catalog::Id` dans ce catalogue d’images/catalogue SVG ou dans ce catalogue de contenu statique doit être unique et ne doit pas inclure de caractères &quot;,&quot;.

## Par défaut {#section-a26e7d83a5ee44b5918baef82ee48e14}

Aucune

## Voir aussi {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribut::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
