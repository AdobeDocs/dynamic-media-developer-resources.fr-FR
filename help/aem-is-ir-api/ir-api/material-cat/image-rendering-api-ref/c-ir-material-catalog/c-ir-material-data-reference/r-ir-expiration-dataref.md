---
description: Temps de mise en cache du client à vivre. Nombre d’heures avant expiration. Permet de gérer la mise en cache du client et du serveur proxy.
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 1%

---


# Expiration{#expiration}

Temps de mise en cache du client à vivre. Nombre d’heures avant expiration. Permet de gérer la mise en cache du client et du serveur proxy.

Le serveur calcule la date et l&#39;heure d&#39;expiration des données de réponse NTTP en ajoutant cette valeur à l&#39;heure et à la date de transmission.

Les navigateurs gèrent les caches à l’aide des heures d’expiration des fichiers. Avant de transmettre une requête au serveur, le navigateur vérifie son cache pour vérifier si le fichier a déjà été téléchargé. Si tel est le cas, et si le fichier n’a pas encore expiré, le navigateur envoie une requête de GET conditionnelle (par exemple avec l’en-tête de requête HTTP If-Modified-Since) plutôt qu’une requête de GET normale. Le serveur a la possibilité de répondre avec un état &quot;304&quot; et de ne pas transmettre l’image. Le navigateur chargera alors simplement le fichier à partir de son cache. Cela peut considérablement augmenter les performances globales pour les données fréquemment consultées.

Le serveur définira l&#39;en-tête de réponse HTTP expires à la date et à l&#39;heure actuelles plus la plus petite des valeurs vignette::Expiration et toutes les valeurs catalog::Expiration pour la vignette et tous les matériaux impliqués dans l&#39;opération de rendu.

L’expiration est définie principalement pour les réponses aux données image. Certains types de réponses seront toujours marqués pour une expiration immédiate (ou marqués comme non pouvant être mis en cache), y compris toutes les réponses d’erreur ou de propriété.

## Propriétés {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Nombre réel, -2, -1, 0 ou supérieur. Nombre d’heures avant expiration depuis la génération de l’image de réponse. La valeur 0 permet de toujours faire expirer l’image de réponse immédiatement, ce qui désactive la mise en cache du client. Définissez sur -1 pour marquer comme `never expire`. Dans ce cas, le serveur renvoie toujours l’état 304 (non modifié) en réponse à des demandes conditionnelles `GET` sans vérifier si le fichier a réellement changé. Définissez cette variable sur -2 pour utiliser la valeur par défaut fournie par `attribute::Expiration`.

## Par défaut {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` est utilisée si le champ n’est pas présent, si la valeur est -2 ou si le champ est vide.

## Voir aussi {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribut ::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
