---
description: Les données d’image intermédiaires générées par les demandes de diffusion d’images et de rendu d’images imbriquées/incorporées peuvent être mises en cache en spécifiant cache=on dans la requête imbriquée/incorporée. Ces données sont stockées dans un format propriétaire dans le cache de données de réponse.
solution: Experience Manager
title: Caches de données auxiliaires
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Caches de données auxiliaires{#auxiliary-data-caches}

Les données d’image intermédiaires générées par les demandes de diffusion d’images et de rendu d’images imbriquées/incorporées peuvent être mises en cache en spécifiant cache=on dans la requête imbriquée/incorporée. Ces données sont stockées dans un format propriétaire dans le cache de données de réponse.

Les images obtenues à partir de serveurs HTTP étrangers sont également stockées dans le cache de données de réponse. Ces images sont validées automatiquement à l’aide de l’utilitaire de validation avant que l’entrée de cache ne soit générée.

Platform Server compile les données du catalogue d’images pour un accès efficace. Ces données sont stockées dans `CS::CatalogCacheFolder`.
