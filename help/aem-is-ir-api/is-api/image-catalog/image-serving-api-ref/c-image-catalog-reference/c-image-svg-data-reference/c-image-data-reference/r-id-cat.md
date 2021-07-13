---
description: Identifiant d’enregistrement du catalogue
solution: Experience Manager
title: ID
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 7%

---

# ID {#id}

Valeur de clé d’index par laquelle les enregistrements dans le fichier de données image sont recherchés par le serveur Platform.

En règle générale, un identifiant d’image court et unique, tel qu’un numéro de SKU, éventuellement avec un suffixe d’image, si un SKU comporte plusieurs images. Il peut également s’agir d’une chaîne plus complexe qui ressemble davantage à un chemin d’accès au fichier, afin de prendre en charge le réajustement facile des sites web avec le serveur d’images.

## Propriétés {#id-properties}

Chaîne de texte. Obligatoire. Clé d’index Principal pour la table de données image. Chaque valeur catalog::Id doit être unique dans le tableau.

## Par défaut {#id-default}

Aucune

## Voir aussi {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
