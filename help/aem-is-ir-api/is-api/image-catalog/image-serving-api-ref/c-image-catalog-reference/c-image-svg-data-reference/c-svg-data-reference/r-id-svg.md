---
title: ID
description: En règle générale, un identificateur court et unique, tel qu’un numéro de SKU, éventuellement avec une sorte de suffixe, par exemple si un SKU comporte plusieurs images ou des variations spécifiques aux paramètres régionaux.
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

En règle générale, un identificateur court et unique, tel qu’un numéro de SKU, éventuellement avec une sorte de suffixe, par exemple si un SKU comporte plusieurs images ou des variations spécifiques aux paramètres régionaux. Il peut également s’agir d’une chaîne plus complexe qui ressemble davantage à un chemin de fichier, afin de faciliter l’ajustement des sites Web avec Image Server.

>[!NOTE]
>
>Les tableaux image et SVG sont fusionnés en un seul tableau lorsque le catalogue d’images est chargé. Les valeurs d’ID doivent être uniques dans les deux tables. L’enregistrement SVG est ignoré si la table d’images contient un enregistrement avec la même valeur d’ID. Le contenu statique est géré dans une table distincte ; Les éléments de contenu statique et les éléments d’image/SVG peuvent donc avoir les mêmes valeurs d’identifiant.

## Propriétés {#section-874a6853f67b4b229341ca76682884ae}

Chaîne de texte. Obligatoire. Identificateur d’enregistrement pour le tableau de données image/SVG ou du contenu statique. Chaque `catalog::Id` valeur de ce catalogue d’images/catalogue SVG ou de ce catalogue de contenu statique doit être unique et ne doit pas inclure les caractères &#39;,&#39;.

## Par défaut {#section-a26e7d83a5ee44b5918baef82ee48e14}

Aucune

## Voir aussi {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute ::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
