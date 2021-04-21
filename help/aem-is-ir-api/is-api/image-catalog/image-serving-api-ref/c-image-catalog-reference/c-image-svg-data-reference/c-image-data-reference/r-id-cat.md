---
description: Identificateur d’enregistrement du catalogue
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---


# ID {#id}

Valeur de clé d’index par laquelle les enregistrements du fichier de données image sont recherchés par le serveur de plateformes.

En règle générale, un identifiant d’image court et unique, tel qu’un numéro SKU, avec éventuellement un suffixe d’image, si un SKU comporte plusieurs images. Il peut également s’agir d’une chaîne plus complexe qui ressemble davantage à un chemin d’accès de fichier, afin de prendre en charge le réaménagement facile des sites Web avec la diffusion d’images.

## Propriétés {#id-properties}

Chaîne de texte. Obligatoire. Clé d’index Principal de la table de données d’image. Chaque valeur catalog::Id doit être unique dans le tableau.

## Par défaut {#id-default}

Aucune

## Voir aussi {#id-seealso}

[attribut::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)