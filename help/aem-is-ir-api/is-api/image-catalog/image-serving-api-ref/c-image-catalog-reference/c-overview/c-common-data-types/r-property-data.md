---
description: Les données de propriété se composent d’une chaîne de texte représentant une ou plusieurs propriétés.
solution: Experience Manager
title: Données de propriété
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Données de propriété{#property-data}

Les données de propriété se composent d’une chaîne de texte représentant une ou plusieurs propriétés.

Une propriété se compose d’un nom de propriété et d’une valeur de propriété, séparés par =.

Plusieurs propriétés sont séparées par des séparateurs de ligne, qui peuvent être `??` ou `<CR><LF>`. Si l’ensemble de la chaîne de données de propriété n’est pas entre guillemets, le serveur remplace chaque occurrence de `??` par `<CR><LF>` avant de transmettre les données au client. Les noms des propriétés peuvent être composés de lettres, de nombres, de &#39;.&#39;, de &#39;-&#39; et de &#39;_&#39;. Les noms des propriétés ne sont pas sensibles à la casse.

Les valeurs de propriété ne doivent pas inclure de séparateurs de ligne.

Voir [Chaîne de texte](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) pour connaître les règles supplémentaires appliquées aux données de propriété.
