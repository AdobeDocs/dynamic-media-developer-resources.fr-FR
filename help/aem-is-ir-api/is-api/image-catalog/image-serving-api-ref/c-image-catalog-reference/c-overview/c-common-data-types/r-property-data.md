---
description: Les données de propriété se composent d’une chaîne de texte représentant une ou plusieurs propriétés.
seo-description: Les données de propriété se composent d’une chaîne de texte représentant une ou plusieurs propriétés.
seo-title: Données de propriété
solution: Experience Manager
title: Données de propriété
topic: Scene7 Image Serving - Image Rendering API
uuid: 7fa6ae70-8d70-41d6-9e47-7df3d616874c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# Données de propriété{#property-data}

Les données de propriété se composent d’une chaîne de texte représentant une ou plusieurs propriétés.

Une propriété se compose d’un nom de propriété et d’une valeur de propriété, séparés par =.

Plusieurs propriétés sont séparées par des séparateurs de lignes, qui peuvent être `??` ou `<CR><LF>`. Si la chaîne de données de propriété entière n’est pas entourée de guillemets, le serveur remplace chaque occurrence de `??` par `<CR><LF>` avant de transmettre les données au client. Les noms de propriété peuvent être composés de lettres, de chiffres, de &quot;.&quot;, de &quot;-&quot; et de &quot;_&quot;. Les noms de propriétés ne sont pas sensibles à la casse.

Les valeurs de propriété ne doivent pas inclure de séparateurs de ligne.

Voir [Chaîne de texte](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) pour connaître les règles supplémentaires appliquées aux données de propriété.
