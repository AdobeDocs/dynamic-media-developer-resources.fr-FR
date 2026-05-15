---
description: Les données de propriété se composent d’une chaîne de texte représentant une ou plusieurs propriétés.
solution: Experience Manager
title: Données de propriété
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
TQID: 'https://experienceleague.adobe.com/jE8U1fgDsG9wdzG4O-BsPHvPOGLXDxZRMdZvL9LuYZE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 0%

---

# Données de propriété{#property-data}

Les données de propriété se composent d’une chaîne de texte représentant une ou plusieurs propriétés.

Une propriété se compose d’un nom de propriété et d’une valeur de propriété, séparés par =.

Plusieurs propriétés sont séparées par des séparateurs de ligne, qui peuvent être `??` ou `<CR><LF>`. Si l’intégralité de la chaîne de données de propriété n’est pas mise entre guillemets, le serveur remplace chaque occurrence de `??` par `<CR><LF>` avant de transmettre les données au client. Les noms des propriétés peuvent être constitués de lettres, de chiffres, de caractères &#39;.&#39;, &#39;-&#39; et &#39;_&#39;. Les noms de propriété ne sont pas sensibles à la casse.

Les valeurs de propriété ne doivent pas inclure de séparateurs de ligne.

Voir [Chaîne de texte](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) pour connaître les règles supplémentaires appliquées aux données de propriété.
