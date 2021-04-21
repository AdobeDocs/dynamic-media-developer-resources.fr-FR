---
description: Les données de propriété se composent d’une chaîne de texte représentant une ou plusieurs propriétés.
solution: Experience Manager
title: Données de propriété
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Données de propriété{#property-data}

Les données de propriété se composent d’une chaîne de texte représentant une ou plusieurs propriétés.

Une propriété se compose d’un nom de propriété et d’une valeur de propriété, séparés par =.

Plusieurs propriétés sont séparées par des séparateurs de lignes, qui peuvent être `??` ou `<CR><LF>`. Si la chaîne de données de propriété entière n’est pas entourée de guillemets, le serveur remplace chaque occurrence de `??` par `<CR><LF>` avant de transmettre les données au client. Les noms de propriété peuvent être composés de lettres, de chiffres, de &quot;.&quot;, de &quot;-&quot; et de &quot;_&quot;. Les noms de propriétés ne sont pas sensibles à la casse.

Les valeurs de propriété ne doivent pas inclure de séparateurs de ligne.

Voir [Chaîne de texte](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) pour connaître les règles supplémentaires appliquées aux données de propriété.
