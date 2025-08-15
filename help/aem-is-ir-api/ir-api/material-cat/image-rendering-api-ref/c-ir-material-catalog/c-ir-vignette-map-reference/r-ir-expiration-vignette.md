---
description: Durée d’expiration du cache client. Nombre d’heures avant l’expiration. Permet de gérer la mise en cache des serveurs client et proxy.
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 3%

---

# Expiration{#expiration}

Durée d’expiration du cache client. Nombre d’heures avant l’expiration. Permet de gérer la mise en cache des serveurs client et proxy.

Voir [catalogue ::Expiration](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md) pour plus de détails.

## Propriétés {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Nombre réel, -2, -1, 0 ou supérieur. Nombre d’heures avant l’expiration du délai depuis que l’image de réponse a été générée. Définissez sur 0 pour toujours faire expirer l’image de réponse immédiatement, ce qui désactive efficacement la mise en cache du client. Défini sur -1 pour marquer comme `never expire`; dans ce cas, le serveur renvoie toujours l’état 403 en réponse aux demandes conditionnelles `GET` sans vérifier si le fichier a réellement changé. Définissez la valeur -2 sur -2 pour utiliser la valeur par défaut fournie par `attribute::Expiration`.

## Par défaut {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` est utilisée si le champ n’est pas présent, si la valeur est -2 ou si le champ est vide.

## Voir aussi {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute ::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [catalogue ::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
