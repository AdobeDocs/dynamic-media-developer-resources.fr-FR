---
description: Les données d’image intermédiaires générées par les demandes imbriquées/incorporées de diffusion d’images et de rendu d’images peuvent être mises en cache en spécifiant cache=on dans la requête imbriquée/incorporée. Ces données sont stockées au format propriétaire dans le cache des données de réponse.
seo-description: Les données d’image intermédiaires générées par les demandes imbriquées/incorporées de diffusion d’images et de rendu d’images peuvent être mises en cache en spécifiant cache=on dans la requête imbriquée/incorporée. Ces données sont stockées au format propriétaire dans le cache des données de réponse.
seo-title: Caches de données auxiliaires
solution: Experience Manager
title: Caches de données auxiliaires
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Caches de données auxiliaires{#auxiliary-data-caches}

Les données d’image intermédiaires générées par les demandes imbriquées/incorporées de diffusion d’images et de rendu d’images peuvent être mises en cache en spécifiant cache=on dans la requête imbriquée/incorporée. Ces données sont stockées au format propriétaire dans le cache des données de réponse.

Les images obtenues à partir de serveurs HTTP étrangers sont également stockées dans le cache de données de réponse. Ces images sont validées automatiquement avec l’utilitaire de validation avant la génération de l’entrée de cache.

Le serveur de plateformes compile les données du catalogue d’images pour un accès efficace. Ces données sont stockées dans `CS::CatalogCacheFolder`.
