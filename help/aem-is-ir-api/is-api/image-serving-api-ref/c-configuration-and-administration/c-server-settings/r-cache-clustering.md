---
description: Utilisez ces paramètres de serveur pour la mise en grappe du cache.
solution: Experience Manager
title: Mise en grappe du cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Mise en grappe du cache{#cache-clustering}

Utilisez ces paramètres de serveur pour la mise en grappe du cache.

## PS ::cacheCluster.hosts - Hôtes {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Liste des adresses IP, séparées par des points-virgules. Incluez les adresses IP de tous les serveurs homologues à partir desquels cet hôte doit obtenir des données de cache. L’adresse IP de l’hôte local peut être incluse pour des raisons de commodité ; Cela permet d’utiliser les mêmes paramètres de configuration pour tous les serveurs de la grappe.

## PS ::cacheCluster.updateLocalCache - Mettre à jour le cache local {#section-154c2c0af4544200a3499232bb130dde}

Définissez sur « Oui » si une entrée de cache fournie par un serveur homologue doit être copiée dans le cache de réponse local.

## PS ::cacheCluster.queryTimeout - Délai de requête {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Lors de la demande d’une entrée de cache à partir de serveurs homologues, le serveur attend qu’un serveur réponde qu’il possède cet élément de données particulier, ou jusqu’à ce que tous les serveurs homologues aient répondu qu’ils n’ont pas l’élément de données, ou jusqu’à ce que le délai spécifié avec ce paramètre (en ms) ait expiré.

## PS ::cacheCluster.fetchTimeout - Récupérer le délai d’expiration {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Spécifie le nombre maximal de msec que le serveur attend que les données de cache réelles soient livrées à partir du serveur homologue. Si les données complètes n’ont pas été livrées avant l’expiration du délai, le serveur suppose que l’homologue est devenu indisponible. L’entrée de cache est ensuite générée localement.
