---
title: Expiration
description: Durée de vie par défaut du cache client.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---

# Expiration{#expiration}

Durée de vie par défaut du cache client. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue particulier ne contiendrait pas de valeur `catalog::Expiration` ou `vignette::Expiration` valide. Ou, si un fichier de vignette ou un fichier de matériau est accessible directement, plutôt qu’au moyen d’un enregistrement de catalogue.

## Propriétés {#section-8e2bade105ec4905ae5c4911f500279f}

Nombre réel, `0` ou plus. Nombre d’heures avant expiration depuis la génération des données de réponse. Définissez cette variable sur `0` pour que l’image de réponse expire toujours immédiatement, ce qui désactive la mise en cache du client. Définissez cette variable sur `-1` pour marquer comme *n’expire jamais*.

## Par défaut {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Hérité de `default::Expiration` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
