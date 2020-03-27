---
description: Durée de vie par défaut du cache client. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contient pas de valeur d’expiration de catalogue ou de vignette valide, ou si un fichier de vignette ou de matériau est directement accessible, plutôt qu’au moyen d’un enregistrement de catalogue.
seo-description: Durée de vie par défaut du cache client. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contient pas de valeur d’expiration de catalogue ou de vignette valide, ou si un fichier de vignette ou de matériau est directement accessible, plutôt qu’au moyen d’un enregistrement de catalogue.
seo-title: Expiration
solution: Experience Manager
title: Expiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b56f9ec-2b25-4e6a-aead-6dad3d2df975
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Expiration{#expiration}

Durée de vie par défaut du cache client. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contient pas de valeur catalog::Expiration ou vignette::Expiration valide, ou si un fichier de vignette ou de matériau est directement accessible, plutôt qu’au moyen d’un enregistrement de catalogue.

## Propriétés {#section-8e2bade105ec4905ae5c4911f500279f}

Nombre réel, 0 ou supérieur. Nombre d’heures avant expiration depuis la génération des données de réponse. Définissez cette valeur sur 0 pour que l’image de réponse arrive à expiration immédiatement, ce qui désactive la mise en cache du client. Définissez cette variable sur -1 pour marquer comme *n’expirant* jamais.

## Par défaut {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Hérité de default::Expiration si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalogue::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
