---
title: ID
description: En règle générale, un identifiant court et unique, tel qu’un numéro de SKU, éventuellement avec un certain type de suffixe, par exemple si un SKU comporte plusieurs images ou des variations spécifiques aux paramètres régionaux.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
TQID: 'https://experienceleague.adobe.com/xPBbjaHO58J-4HFnChD1ybEVoE2AbRZuFVA8nbquEvg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 3%

---

# ID{#id}

En règle générale, un identifiant court et unique, tel qu’un numéro de SKU, éventuellement avec un certain type de suffixe, par exemple si un SKU comporte plusieurs images ou des variations spécifiques aux paramètres régionaux. Peut également être une chaîne plus complexe qui ressemble davantage à un chemin d’accès au fichier, pour prendre en charge la modernisation facile des sites web avec la diffusion d’images.

>[!NOTE]
>
>Les tableaux image et SVG sont fusionnés en un seul tableau lors du chargement du catalogue d’images. Les valeurs d’ID doivent être uniques pour les deux tables. L’enregistrement SVG est ignoré si la table d’images contient un enregistrement avec la même valeur d’identifiant. Le contenu statique est géré avec un tableau distinct ; les éléments de contenu statique et les éléments d’image/SVG peuvent donc avoir les mêmes valeurs d’ID.

## Propriétés {#section-874a6853f67b4b229341ca76682884ae}

Chaîne de texte. Obligatoire. Identifiant d’enregistrement pour le tableau de données image/SVG ou contenu statique. Chaque valeur `catalog::Id` dans ce catalogue d’images/catalogue SVG ou dans ce catalogue de contenu statique doit être unique et ne doit pas inclure de caractères « , ».

## Par défaut {#section-a26e7d83a5ee44b5918baef82ee48e14}

Aucune

## Voir aussi {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
