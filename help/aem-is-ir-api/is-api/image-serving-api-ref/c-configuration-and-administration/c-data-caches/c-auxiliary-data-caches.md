---
description: Les données d’image intermédiaires produites par les requêtes de diffusion d’images et de rendu d’images imbriquées/intégrées peuvent être mises en cache en spécifiant cache=on dans la requête imbriquée/incorporée. Ces données sont stockées dans un format propriétaire dans le cache de données de réponse.
solution: Experience Manager
title: Caches de données auxiliaires
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
TQID: 'https://experienceleague.adobe.com/oRZFSXKaBE9q7liBPRVCheL-NPTriPJkWZFqgMBcoaQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# Caches de données auxiliaires{#auxiliary-data-caches}

Les données d’image intermédiaires produites par les requêtes de diffusion d’images et de rendu d’images imbriquées/intégrées peuvent être mises en cache en spécifiant cache=on dans la requête imbriquée/incorporée. Ces données sont stockées dans un format propriétaire dans le cache de données de réponse.

Les images obtenues à partir de serveurs HTTP étrangers sont également stockées dans le cache de données de réponse. Ces images sont automatiquement validées avec l’utilitaire de validation avant la génération de l’entrée de cache.

Le [!DNL Platform Server] compile les données du catalogue d’images pour un accès efficace. Ces données sont stockées dans `CS::CatalogCacheFolder`.
