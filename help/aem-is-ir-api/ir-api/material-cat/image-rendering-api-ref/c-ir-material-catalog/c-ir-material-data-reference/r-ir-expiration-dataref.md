---
title: Expiration
description: Durée d’expiration du cache client. Nombre d’heures avant l’expiration. Permet de gérer la mise en cache des serveurs client et proxy.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---

# Expiration{#expiration}

Durée d’expiration du cache client. Nombre d’heures avant l’expiration. Permet de gérer la mise en cache des serveurs client et proxy.

Le serveur calcule l’heure et la date d’expiration des données de réponse NTTP en ajoutant cette valeur à l’heure et à la date de transmission.

Les navigateurs gèrent les caches en utilisant les délais d’expiration des fichiers. Avant de transmettre une requête au serveur, le navigateur vérifie son cache pour voir si le fichier a déjà été téléchargé. Si c’est le cas, et si le fichier n’a pas encore expiré, le navigateur envoie une demande de GET conditionnelle (par exemple avec l’en-tête de requête HTTP If-Modified-Since ) plutôt qu’une demande GET normale. Le serveur a la possibilité de répondre avec un statut &#39;304&#39; et de ne pas transmettre l’image. Le navigateur charge alors simplement le fichier à partir de son cache. Cela peut considérablement accroître les performances globales des données fréquemment consultées.

Le serveur définit l’en-tête de réponse HTTP expires sur la date/heure actuelle plus la plus petite des valeurs vignette ::Expiration et toutes les valeurs catalog ::Expiration pour la vignette et tous les matériaux impliqués dans l’opération de rendu.

L’expiration est définie principalement pour les réponses de données image. Certains types de réponses sont toujours marqués pour expiration immédiate (ou marqués comme ne pouvant pas être mis en cache), y compris toutes les réponses d’erreur ou les réponses de propriété.

## Propriétés {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Nombre réel, -2, -1, 0 ou supérieur. Nombre d’heures avant l’expiration du délai depuis que l’image de réponse a été générée. Définissez sur 0 pour toujours faire expirer l’image de réponse immédiatement, ce qui désactive efficacement la mise en cache du client. Définissez la valeur -1 sur -1 pour marquer comme `never expire`. Dans ce cas, le serveur renvoie toujours l’état 304 (non modifié) en réponse aux demandes conditionnelles `GET` sans vérifier si le fichier a réellement changé. Définissez la valeur -2 sur -2 pour utiliser la valeur par défaut fournie par `attribute::Expiration`.

## Par défaut {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` est utilisée si le champ n’est pas présent, si la valeur est -2 ou si le champ est vide.

## Voir aussi {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute ::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [vignette ::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
