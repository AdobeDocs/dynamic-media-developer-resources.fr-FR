---
description: Identifiant d’enregistrement du catalogue
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 6%

---

# ID {#id}

Valeur de clé d’index par laquelle les enregistrements du fichier de données image sont recherchés par le [!DNL Platform Server].

En règle générale, un identifiant d’image court et unique, tel qu’un numéro de SKU, éventuellement avec un suffixe d’image, si un SKU comporte plusieurs images. Il peut également s’agir d’une chaîne plus complexe qui ressemble davantage à un chemin d’accès au fichier, afin de prendre en charge le réajustement facile des sites web avec le serveur d’images.

## Propriétés {#id-properties}

Chaîne de texte. Obligatoire. Clé d’index de Principal pour la table de données image. Chaque valeur catalog::Id doit être unique dans le tableau.

## Par défaut {#id-default}

Aucune

## Voir aussi {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
