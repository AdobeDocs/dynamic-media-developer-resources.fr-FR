---
description: Les données d’image intermédiaires générées par les demandes imbriquées/incorporées de diffusion d’images et de rendu d’image peuvent être mises en cache en spécifiant cache=on dans la demande imbriquée/incorporée. Ces données sont stockées dans un format propriétaire dans le cache de données de réponse.
seo-description: Les données d’image intermédiaires générées par les demandes imbriquées/incorporées de diffusion d’images et de rendu d’image peuvent être mises en cache en spécifiant cache=on dans la demande imbriquée/incorporée. Ces données sont stockées dans un format propriétaire dans le cache de données de réponse.
seo-title: Caches de données auxiliaires
solution: Experience Manager
title: Caches de données auxiliaires
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Caches de données auxiliaires{#auxiliary-data-caches}

Les données d’image intermédiaires générées par les demandes imbriquées/incorporées de diffusion d’images et de rendu d’image peuvent être mises en cache en spécifiant cache=on dans la demande imbriquée/incorporée. Ces données sont stockées dans un format propriétaire dans le cache de données de réponse.

Les images obtenues à partir de serveurs HTTP étrangers sont également stockées dans le cache de données de réponse. Ces images sont validées automatiquement avec l’utilitaire de validation avant la génération de l’entrée de cache.

Platform Server compile des données de catalogue d’images pour un accès efficace. Ces données sont stockées dans `CS::CatalogCacheFolder`.
