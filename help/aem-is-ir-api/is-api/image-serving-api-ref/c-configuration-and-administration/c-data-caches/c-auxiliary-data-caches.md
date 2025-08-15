---
description: Les données d’image intermédiaires produites par les demandes de service d’image et de rendu d’image imbriquées/intégrées peuvent être mises en cache en spécifiant cache=on dans la requête imbriquée/intégrée. Ces données sont stockées dans un format propriétaire dans le cache des données de réponse.
solution: Experience Manager
title: Caches de données auxiliaires
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Caches de données auxiliaires{#auxiliary-data-caches}

Les données d’image intermédiaires produites par les demandes de service d’image et de rendu d’image imbriquées/intégrées peuvent être mises en cache en spécifiant cache=on dans la requête imbriquée/intégrée. Ces données sont stockées dans un format propriétaire dans le cache des données de réponse.

Les images obtenues à partir de serveurs HTTP étrangers sont également stockées dans le cache de données de réponse. Ces images sont validées automatiquement avec l’utilitaire de validation avant que l’entrée de cache ne soit générée.

La [!DNL Platform Server] compile les données du catalogue d’images pour un accès efficace. Ces données sont stockées dans `CS::CatalogCacheFolder`.
