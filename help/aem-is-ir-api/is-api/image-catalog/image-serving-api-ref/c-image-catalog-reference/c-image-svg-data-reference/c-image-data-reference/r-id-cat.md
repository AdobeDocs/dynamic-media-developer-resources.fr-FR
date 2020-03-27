---
description: Identificateur d’enregistrement du catalogue
solution: Experience Manager
title: ID
topic: Scene7 Image Serving - Image Rendering API
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
translation-type: tm+mt
source-git-commit: 7d3902803d42f5d479dd04ac9470a4088809f3d6

---


# ID {#id}

Valeur de clé d’index par laquelle les enregistrements du fichier de données image sont recherchés par le serveur de plateformes.

En règle générale, un identifiant d’image court et unique, tel qu’un numéro SKU, avec éventuellement un suffixe d’image, si un SKU comporte plusieurs images. Il peut également s’agir d’une chaîne plus complexe qui ressemble davantage à un chemin d’accès de fichier, afin de prendre en charge le réajustement facile des sites Web avec la diffusion d’images.

## Propriétés {#id-properties}

Chaîne de texte. Obligatoire. Clé d’index principale de la table de données d’image. Chaque valeur catalog::Id doit être unique dans le tableau.

## Par défaut {#id-default}

Aucune

## Voir aussi {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)