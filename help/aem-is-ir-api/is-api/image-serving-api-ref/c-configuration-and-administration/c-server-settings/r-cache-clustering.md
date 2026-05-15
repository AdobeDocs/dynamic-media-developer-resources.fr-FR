---
description: Utilisez ces paramètres de serveur pour la mise en grappe du cache.
solution: Experience Manager
title: Mise en cluster du cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
TQID: 'https://experienceleague.adobe.com/4SJmK1ILgnCBqYjjQcEnz0SVRzQfsY9mD05Xpd1ssnw'
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
source-wordcount: 200
ht-degree: 0%

---

# Mise en cluster du cache{#cache-clustering}

Utilisez ces paramètres de serveur pour la mise en grappe du cache.

## PS::cacheCluster.hosts - Hôtes {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Liste d’adresses IP, séparées par des points-virgules. Incluez les adresses IP de tous les serveurs de pairs à partir desquels cet hôte doit obtenir des données de cache. L’adresse IP de l’hôte local peut être incluse pour des raisons pratiques ; cela permet d’obtenir les mêmes paramètres de configuration pour tous les serveurs du cluster.

## PS::cacheCluster.updateLocalCache - Mise à jour du cache local {#section-154c2c0af4544200a3499232bb130dde}

Définissez sur « Oui » si une entrée de cache fournie par un serveur homologue doit être copiée dans le cache de réponse local.

## PS::cacheCluster.queryTimeout - Délai d’expiration de la requête {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Lors de la demande d’une entrée de cache aux serveurs homologues, le serveur attend qu’un serveur réponde qu’il dispose de cet élément de données particulier, ou que tous les serveurs homologues répondent qu’ils ne disposent pas de l’élément de données, ou que le délai spécifié avec ce paramètre (en ms) ait expiré.

## PS::cacheCluster.fetchTimeout - Délai de récupération {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Indique le nombre maximal de ms que le serveur attend pour que les données de cache réelles soient diffusées à partir du serveur homologue. Si les données complètes n’ont pas été diffusées avant l’expiration du délai, le serveur suppose que l’homologue n’est plus disponible. L’entrée du cache est ensuite générée localement.
