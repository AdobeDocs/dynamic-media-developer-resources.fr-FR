---
description: Temps de mise en cache du client par défaut à vivre. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contiendrait pas de valeur d’expiration de catalogue ou de vignette valide, ou si un fichier de vignette ou de matériau est directement accessible, plutôt qu’au moyen d’un enregistrement de catalogue.
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---


# Expiration{#expiration}

Temps de mise en cache du client par défaut à vivre. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contient pas de valeur catalog::Expiration ou vignette::Expiration valide, ou si un fichier de vignette ou de matériau est directement accessible, plutôt que par le biais d’un enregistrement de catalogue.

## Propriétés {#section-8e2bade105ec4905ae5c4911f500279f}

Nombre réel, 0 ou supérieur. Nombre d&#39;heures avant expiration depuis la génération des données de réponse. La valeur 0 permet de toujours faire expirer l’image de réponse immédiatement, ce qui désactive la mise en cache du client. Définissez sur -1 pour marquer comme *n’expire jamais*.

## Par défaut {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Hérité de default::Expiration si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalogue ::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
