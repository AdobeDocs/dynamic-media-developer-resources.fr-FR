---
description: Temps de mise en cache du client pour vivre. Nombre d’heures avant expiration. Permet de gérer la mise en cache du client et du serveur proxy.
seo-description: Temps de mise en cache du client pour vivre. Nombre d’heures avant expiration. Permet de gérer la mise en cache du client et du serveur proxy.
seo-title: Expiration
solution: Experience Manager
title: Expiration
topic: Scene7 Image Serving - Image Rendering API
uuid: fa267728-9a36-4705-97d6-d567148fc2d7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Expiration{#expiration}

Temps de mise en cache du client pour vivre. Nombre d’heures avant expiration. Permet de gérer la mise en cache du client et du serveur proxy.

See ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)` for details.

## Propriétés {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Nombre réel, -2, -1, 0 ou supérieur. Nombre d’heures avant expiration depuis la génération de l’image de réponse. Définissez cette valeur sur 0 pour que l’image de réponse arrive à expiration immédiatement, ce qui désactive la mise en cache du client. Définissez sur -1 pour marquer comme `never expire`; dans ce cas, le serveur renvoie toujours l’état 403 en réponse aux `GET` requêtes conditionnelles sans vérifier si le fichier a réellement changé. Définissez cette variable sur -2 pour utiliser la valeur par défaut fournie par `attribute::Expiration`.

## Par défaut {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` est utilisée si le champ n’est pas présent, si la valeur est -2 ou si le champ est vide.

## Voir aussi {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribut::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [catalogue::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
