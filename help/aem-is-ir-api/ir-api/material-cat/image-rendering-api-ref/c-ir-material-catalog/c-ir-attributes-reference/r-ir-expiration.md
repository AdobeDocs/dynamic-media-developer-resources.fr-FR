---
title: Expiration
description: Délai d’expiration par défaut du cache client.
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

Délai d’expiration par défaut du cache client. Fournit un intervalle d’expiration par défaut dans le cas où un enregistrement de catalogue particulier ne contient pas de valeur valide `catalog::Expiration` ou `vignette::Expiration` . Ou, si un fichier de vignette ou un fichier matériel est accessible directement, plutôt que par le biais d’une notice de catalogue.

## Propriétés {#section-8e2bade105ec4905ae5c4911f500279f}

Nombre réel, `0` ou supérieur. Nombre d’heures avant expiration depuis que les données de réponse ont été générées. Défini sur `0` pour toujours expirer l’image de réponse immédiatement, ce qui désactive efficacement la mise en cache du client. Définissez cette valeur sur `-1` pour marquer comme n’ayant *jamais expiration*.

## Par défaut {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Hérité de `default::Expiration` si non défini ou si vide.

## Voir aussi {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog ::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vignette ::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
