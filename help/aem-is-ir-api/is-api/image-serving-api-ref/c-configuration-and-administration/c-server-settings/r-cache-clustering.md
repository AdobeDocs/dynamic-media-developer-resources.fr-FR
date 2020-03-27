---
description: Utilisez ces paramètres de serveur pour la mise en grappe du cache.
seo-description: Utilisez ces paramètres de serveur pour la mise en grappe du cache.
seo-title: Mise en grappe du cache
solution: Experience Manager
title: Mise en grappe du cache
topic: Scene7 Image Serving - Image Rendering API
uuid: ed6335d7-26c9-45d8-95f6-6c05e788e449
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Mise en grappe du cache{#cache-clustering}

Utilisez ces paramètres de serveur pour la mise en grappe du cache.

## PS::cacheCluster.hosts - Hôtes {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

 des adresses IP, séparés par des points-virgules. Incluez les adresses IP de tous les serveurs homologues à partir desquels cet hôte doit obtenir des données de cache. L&#39;adresse IP de l&#39;hôte local peut être incluse à des fins pratiques; cela permet les mêmes paramètres de configuration pour tous les serveurs de la grappe.

## PS::cacheCluster.updateLocalCache - Mettre à jour le cache local {#section-154c2c0af4544200a3499232bb130dde}

Définissez cette variable sur Oui si une entrée de cache fournie par un serveur homologue doit être copiée dans le cache de réponse local.

## PS::cacheCluster.queryTimeout - Délai d’expiration {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Lors de la demande d’une entrée de cache auprès de serveurs homologues, le serveur attend qu’un serveur réponde qu’il possède cet élément de données particulier, ou que tous les serveurs homologues répondent qu’ils n’ont pas l’élément de données, ou que le délai spécifié avec ce paramètre (en msec) ait expiré.

## PS::cacheCluster.fetchTimeout - Délai de récupération {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Spécifie le nombre maximal de msec que le serveur attend pour que les données de cache réelles soient diffusées à partir du serveur homologue. Si les données complètes n’ont pas été remises avant l’expiration du délai d’attente, le serveur suppose que le pair est devenu indisponible. L’entrée de cache est alors générée localement.
