---
description: Utilisez ces paramètres de serveur pour la mise en grappe du cache.
solution: Experience Manager
title: Mise en grappe du cache
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Mise en grappe du cache{#cache-clustering}

Utilisez ces paramètres de serveur pour la mise en grappe du cache.

## PS::cacheCluster.hosts - Hôtes {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Liste des adresses IP, séparées par des points-virgules. Incluez les adresses IP de tous les serveurs pairs à partir desquels cet hôte doit obtenir des données de cache. L’adresse IP de l’hôte local peut être incluse à des fins pratiques ; cela permet d’utiliser les mêmes paramètres de configuration pour tous les serveurs de la grappe.

## PS::cacheCluster.updateLocalCache - Mettre à jour le cache local {#section-154c2c0af4544200a3499232bb130dde}

Définissez cette variable sur &quot;Oui&quot; si une entrée de cache fournie par un serveur homologue doit être copiée dans le cache de réponse local.

## PS::cacheCluster.queryTimeout - Query Timeout {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Lors de la demande d’une entrée de cache de la part des serveurs pairs, le serveur attend qu’un serveur réponde lorsqu’il possède cet élément de données particulier, ou jusqu’à ce que tous les serveurs pairs aient répondu qu’ils ne disposent pas de l’élément de données, ou jusqu’à ce que le délai spécifié avec ce paramètre (en ms) expire.

## PS::cacheCluster.fetchTimeout - Fetch Timeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Spécifie le nombre maximal de msec pendant lesquels le serveur attend que les données de cache réelles soient diffusées à partir du serveur pair. Si les données complètes n’ont pas été diffusées avant l’expiration du délai d’expiration, le serveur suppose que le pair est devenu indisponible. L’entrée de cache est ensuite générée localement.
