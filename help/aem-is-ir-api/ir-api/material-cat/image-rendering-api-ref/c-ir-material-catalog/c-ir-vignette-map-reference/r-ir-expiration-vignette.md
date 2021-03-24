---
description: Temps de mise en cache du client à vivre. Nombre d’heures avant expiration. Permet de gérer la mise en cache du client et du serveur proxy.
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---


# Expiration{#expiration}

Temps de mise en cache du client à vivre. Nombre d’heures avant expiration. Permet de gérer la mise en cache du client et du serveur proxy.

Voir ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)` pour plus de détails.

## Propriétés {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Nombre réel, -2, -1, 0 ou supérieur. Nombre d’heures avant expiration depuis la génération de l’image de réponse. La valeur 0 permet de toujours faire expirer l’image de réponse immédiatement, ce qui désactive la mise en cache du client. Définissez sur -1 pour marquer comme `never expire`; dans ce cas, le serveur renvoie toujours l’état 403 en réponse aux requêtes conditionnelles `GET` sans vérifier si le fichier a réellement changé. Définissez cette variable sur -2 pour utiliser la valeur par défaut fournie par `attribute::Expiration`.

## Par défaut {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` est utilisée si le champ n’est pas présent, si la valeur est -2 ou si le champ est vide.

## Voir aussi {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribut ::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catalogue::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
