---
description: Utilisez ces paramètres de serveur pour la mise en grappe du cache.
solution: Experience Manager
title: Mise en grappe du cache
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Mise en grappe du cache {#cache-clustering}

Utilisez ces paramètres de serveur pour la mise en grappe du cache.

## PS::cacheCluster.hosts - Hôtes {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Liste des adresses IP, séparées par des points-virgules. Incluez les adresses IP de tous les serveurs homologues à partir desquels cet hôte doit obtenir des données de cache. L&#39;adresse IP de l&#39;hôte local peut être incluse à des fins pratiques ; cela permet les mêmes paramètres de configuration pour tous les serveurs de la grappe.

## PS::cacheCluster.updateLocalCache - Mettre à jour le cache local {#section-154c2c0af4544200a3499232bb130dde}

Définissez sur &quot;Oui&quot; si une entrée de cache fournie par un serveur homologue doit être copiée dans le cache de réponse local.

## PS::cacheCluster.queryTimeout - Délai d&#39;expiration de la Requête {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Lorsque vous demandez une entrée de cache à des serveurs homologues, le serveur attend qu&#39;un serveur réponde qu&#39;il possède cet élément de données particulier, ou que tous les serveurs homologues répondent qu&#39;ils n&#39;ont pas l&#39;élément de données, ou que le temps spécifié avec ce paramètre (en msec) soit écoulé.

## PS::cacheCluster.fetchTimeout - Délai d&#39;extraction {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Spécifie le nombre maximal de msec pendant lequel le serveur attend que les données de cache réelles soient livrées à partir du serveur homologue. Si les données complètes n’ont pas été remises avant l’expiration du délai d’attente, le serveur suppose que l’homologue est devenu indisponible. L’entrée de cache est ensuite générée localement.
