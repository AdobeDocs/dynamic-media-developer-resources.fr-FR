---
description: Durée de vie du cache client. Nombre d'heures avant expiration. Utilisé pour gérer la mise en cache du client et du serveur proxy.
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
TQID: 'https://experienceleague.adobe.com/VHARdBKoak-pB54FrPO6u0Gpmd-1sQZUF-78j3ixB2U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 3%

---

# Expiration{#expiration}

Durée de vie du cache client. Nombre d&#39;heures avant expiration. Utilisé pour gérer la mise en cache du client et du serveur proxy.

Voir [catalog::Expiration](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md) pour plus d’informations.

## Propriétés {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Nombre réel, -2, -1, 0 ou supérieur. Nombre d’heures avant expiration depuis la génération de l’image de réponse. Définissez la valeur sur 0 pour que l’image de réponse expire immédiatement, ce qui désactive efficacement la mise en cache du client. Définissez la valeur sur -1 pour marquer comme `never expire` ; dans ce cas, le serveur renvoie toujours le statut 403 en réponse aux demandes de `GET` conditionnelles sans vérifier si le fichier a réellement changé. Définissez la valeur sur -2 pour utiliser la valeur par défaut fournie par `attribute::Expiration`.

## Par défaut {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` est utilisé si le champ n’est pas présent, si la valeur est -2 ou si le champ est vide.

## Voir aussi {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
