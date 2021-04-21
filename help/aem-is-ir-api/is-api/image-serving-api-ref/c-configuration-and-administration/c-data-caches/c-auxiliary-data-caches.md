---
description: Les données d’image intermédiaires générées par les demandes imbriquées/incorporées de diffusion d’images et de rendu d’image peuvent être mises en cache en spécifiant cache=on dans la demande imbriquée/incorporée. Ces données sont stockées dans un format propriétaire dans le cache de données de réponse.
solution: Experience Manager
title: Caches de données auxiliaires
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# Caches de données auxiliaires{#auxiliary-data-caches}

Les données d’image intermédiaires générées par les demandes imbriquées/incorporées de diffusion d’images et de rendu d’image peuvent être mises en cache en spécifiant cache=on dans la demande imbriquée/incorporée. Ces données sont stockées dans un format propriétaire dans le cache de données de réponse.

Les images obtenues à partir de serveurs HTTP étrangers sont également stockées dans le cache de données de réponse. Ces images sont validées automatiquement avec l’utilitaire de validation avant la génération de l’entrée de cache.

Platform Server compile des données de catalogue d’images pour un accès efficace. Ces données sont stockées dans `CS::CatalogCacheFolder`.
