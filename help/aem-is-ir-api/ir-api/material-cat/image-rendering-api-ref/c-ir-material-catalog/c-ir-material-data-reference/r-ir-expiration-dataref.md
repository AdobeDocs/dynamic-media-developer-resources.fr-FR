---
title: Expiration
description: Durée de vie du cache client. Nombre d'heures avant expiration. Utilisé pour gérer la mise en cache du client et du serveur proxy.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
TQID: 'https://experienceleague.adobe.com/dFnSsD8mmC0aPefS3Z0GujF1A-p1nCQyiNpzMXxOBEQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 1%

---

# Expiration{#expiration}

Durée de vie du cache client. Nombre d&#39;heures avant expiration. Utilisé pour gérer la mise en cache du client et du serveur proxy.

Le serveur calcule la date/l’heure d’expiration des données de réponse NTP en ajoutant cette valeur à la date/l’heure de transmission.

Les navigateurs gèrent les caches à l’aide des délais d’expiration des fichiers. Avant de transmettre une requête au serveur, le navigateur vérifie son cache pour voir si le fichier a déjà été téléchargé. Si tel est le cas, et si le fichier n’a pas encore expiré, le navigateur envoie une requête GET conditionnelle (par exemple avec l’en-tête de requête HTTP If-Modified-Since ) plutôt qu’une requête GET classique. Le serveur a la possibilité de répondre avec un statut « 304 » et de ne pas transmettre l’image. Le navigateur charge ensuite simplement le fichier à partir de son cache. Cela peut augmenter considérablement les performances globales des données fréquemment consultées.

Le serveur définit l’en-tête de réponse HTTP d’expiration sur la date/l’heure actuelle, plus la plus petite des valeurs vignette::Expiration et catalogue::Expiration pour la vignette et tous les matériaux impliqués dans l’opération de rendu.

L’expiration est principalement définie pour les réponses de données d’image. Certains types de réponses sont toujours marqués pour une expiration immédiate (ou marqués comme ne pouvant pas être mis en cache), y compris toutes les réponses d’erreur ou de propriété.

## Propriétés {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Nombre réel, -2, -1, 0 ou supérieur. Nombre d’heures avant expiration depuis la génération de l’image de réponse. Définissez la valeur sur 0 pour que l’image de réponse expire immédiatement, ce qui désactive efficacement la mise en cache du client. Définissez-le sur -1 pour marquer comme `never expire`. Dans ce cas, le serveur renvoie toujours le statut 304 (non modifié) en réponse aux demandes de `GET` conditionnelles sans vérifier si le fichier a réellement changé. Définissez la valeur sur -2 pour utiliser la valeur par défaut fournie par `attribute::Expiration`.

## Par défaut {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` est utilisé si le champ n’est pas présent, si la valeur est -2 ou si le champ est vide.

## Voir aussi {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
