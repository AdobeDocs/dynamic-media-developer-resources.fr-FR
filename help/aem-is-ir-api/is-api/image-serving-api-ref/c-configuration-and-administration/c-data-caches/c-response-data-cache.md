---
title: Cache de données de réponse
description: Le  [!DNL Platform Server]  met en cache toutes les images de réponse et certaines données texte sur le disque, sauf si une requête est marquée comme non pouvant être mise en cache.
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

Le [!DNL Platform Server] met en cache toutes les images de réponse et certaines données texte sur le disque, sauf si une requête est marquée comme non mise en cache.

L’emplacement du cache disque de [!DNL Platform Server] est défini avec `PS::cache.rootPaths`.

Pour les applications présentant des taux d’accès au cache élevés, vous pouvez augmenter les performances et la capacité du serveur en répartissant le cache de données de réponse entre plusieurs périphériques de disque. Pour ce faire, créez un dossier racine de cache sur chaque disque et enregistrez-le dans `PS::cache.rootPaths`.

`PS::cache.maxSize` spécifie la taille totale de toutes les entrées de cache, sans tenir compte de la surcharge du système de fichiers. La quantité d’espace disque requise dépend des propriétés du système de fichiers, telles que la taille du bloc de disque, et le nombre d’entrées de cache. Réservez deux fois plus d’espace disque pour le cache disque HTTP que la quantité spécifiée par `PS::cache.maxSize`. Un algorithme récemment utilisé est utilisé pour maintenir la quantité de données mises en cache dans la limite.

Outre `PS::cache.maxSize`, le cache de réponse est également géré en limitant le nombre maximal d’entrées de cache avec `PS::cache.maxEntries`. Sous Linux®, ce paramètre doit spécifier une valeur ne dépassant pas le nombre d’informations disponibles sur la partition du cache.

>[!NOTE]
>
>[!DNL Platform Server] conserve un index de cache en mémoire. La taille de cet index est de 32 octets fois la valeur de `PS::cache.maxEntries`. Si nécessaire, augmentez la taille du tas [!DNL Platform Server] pour accueillir des caches plus grands.

Le système utilise un fichier d’index de cache qui est enregistré sur le disque lorsque le serveur est arrêté de manière ordonnée. En cas d’événements inattendus, tels qu’une panne de courant, ce fichier peut ne pas être enregistré. En outre, il peut s’écouler plusieurs minutes avant que [!DNL Platform Server] ne soit prêt.
