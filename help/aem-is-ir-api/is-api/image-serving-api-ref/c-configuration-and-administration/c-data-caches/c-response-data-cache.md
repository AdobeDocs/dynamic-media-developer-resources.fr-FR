---
title: Cache de données de réponse
description: La [!DNL Platform Server] mise en cache de toutes les images de réponse et de certaines données textuelles sur le disque, sauf si une demande est marquée comme non pouvant être mise en cache.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Cache de données de réponse{#response-data-cache}

Le [!DNL Platform Server] met en cache toutes les images de réponse et certaines données textuelles sur le disque, sauf si une demande est marquée comme non pouvant être mise en cache.

L’emplacement du [!DNL Platform Server]cache disque de est défini avec `PS::cache.rootPaths`.

Pour les applications qui ont des taux d’accès au cache élevés, vous pouvez augmenter les performances et la capacité du serveur en répartissant le cache de données de réponse entre plusieurs unités de disque. Pour ce faire, créez un dossier racine de cache sur chaque disque et enregistrez-les dans `PS::cache.rootPaths`.

Le `PS::cache.maxSize` spécifie la taille totale de toutes les entrées du cache, sans tenir compte de la surcharge du système de fichiers. La quantité d’espace disque requise dépend des propriétés du système de fichiers, telles que la taille du bloc de disque, et du nombre d’entrées de cache. Réservez deux fois plus d’espace disque pour le cache disque HTTP que la quantité spécifiée par `PS::cache.maxSize`. Un algorithme le moins récemment utilisé est utilisé pour maintenir la quantité de données mises en cache dans la limite.

En plus de `PS::cache.maxSize`, le cache de réponse est également géré en limitant le nombre maximal d’entrées de cache avec `PS::cache.maxEntries`. Sous Linux®, ce paramètre doit spécifier une valeur non supérieure au nombre d’inodes disponibles sur la partition de cache.

>[!NOTE]
>
>Le [!DNL Platform Server] gère un index du cache en mémoire. La taille de cet index est de 32 octets fois la valeur de `PS::cache.maxEntries`. Si nécessaire, augmentez la taille du tas pour accueillir des [!DNL Platform Server] caches plus volumineux.

Le système utilise un fichier d’index de cache qui est enregistré sur le disque lorsque le serveur est arrêté de manière ordonnée. En cas d’événements inattendus tels qu’une panne de courant, ce fichier peut ne pas être enregistré. En outre, cela peut prendre plusieurs minutes pour que le [!DNL Platform Server] soit prêt.
