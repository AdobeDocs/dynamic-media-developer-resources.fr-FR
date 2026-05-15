---
title: Cache des données de réponse
description: Le  [!DNL Platform Server]  met en cache toutes les images de réponse et certaines données de texte sur le disque, sauf si une requête est marquée comme ne pouvant pas être mise en cache.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
TQID: 'https://experienceleague.adobe.com/zxZqRHFCMKKDxOBb35IEZWEhTFhknDgCKcYatA6lqGs'
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
source-wordcount: 282
ht-degree: 0%

---

# Cache des données de réponse{#response-data-cache}

Le [!DNL Platform Server] met en cache toutes les images de réponse et certaines données de texte sur le disque, sauf si une requête est marquée comme ne pouvant pas être mise en cache.

L’emplacement du cache disque du [!DNL Platform Server] est défini avec `PS::cache.rootPaths`.

Pour les applications qui présentent des taux d’accès au cache élevés, vous pouvez augmenter les performances et la capacité du serveur en distribuant le cache de données de réponse entre plusieurs périphériques de disque. Pour ce faire, créez un dossier racine de cache sur chaque disque et enregistrez-le dans `PS::cache.rootPaths`.

Le `PS::cache.maxSize` spécifie la taille totale de toutes les entrées du cache, sans tenir compte de la surcharge du système de fichiers. La quantité d’espace disque requise dépend des propriétés du système de fichiers, telles que la taille du bloc de disque, et du nombre d’entrées du cache. Réservez deux fois plus d’espace disque pour le cache disque HTTP que la quantité spécifiée par `PS::cache.maxSize`. Un algorithme utilisé le moins récemment est utilisé pour maintenir la quantité de données mises en cache dans la limite.

En plus de `PS::cache.maxSize`, le cache de réponse est également géré en limitant le nombre maximal d’entrées de cache avec `PS::cache.maxEntries`. Sous Linux®, ce paramètre doit spécifier une valeur ne dépassant pas le nombre d’inodes disponibles sur la partition de cache.

>[!NOTE]
>
>Le [!DNL Platform Server] conserve un index de cache en mémoire. La taille de cet index est égale à 32 octets multipliés par la valeur de `PS::cache.maxEntries`. Augmentez la taille du tas [!DNL Platform Server] pour accueillir des caches plus volumineux, si nécessaire.

Le système utilise un fichier d’index de cache qui est enregistré sur le disque lorsque le serveur est arrêté de manière ordonnée. En cas d’événements inattendus, comme une coupure de courant, ce fichier risque de ne pas être enregistré. En outre, il peut s’écouler plusieurs minutes avant que le [!DNL Platform Server] ne soit prêt.
