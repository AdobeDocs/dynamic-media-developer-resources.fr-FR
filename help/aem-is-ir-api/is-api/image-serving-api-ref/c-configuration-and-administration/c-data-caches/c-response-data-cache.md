---
description: Le serveur de plateformes met en cache toutes les images de réponse et certaines données de texte sur le disque, sauf si une requête est marquée comme non pouvant être mise en cache.
solution: Experience Manager
title: Cache de données de réponse
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# Cache de données de réponse{#response-data-cache}

Le serveur de plateformes met en cache toutes les images de réponse et certaines données de texte sur le disque, sauf si une requête est marquée comme non pouvant être mise en cache.

L&#39;emplacement du cache disque de Platform Server est défini avec `PS::cache.rootPaths`.

Pour les applications présentant un taux d&#39;accès élevé au cache, vous pouvez augmenter les performances et la capacité du serveur en répartissant le cache de données de réponse entre plusieurs périphériques de disque. Pour ce faire, créez un dossier racine de cache sur chaque disque et enregistrez-le dans `PS::cache.rootPaths`.

`PS::cache.maxSize` indique la taille totale de toutes les entrées de cache, sans tenir compte de la surcharge du système de fichiers. La quantité d&#39;espace disque réellement requise dépend des propriétés du système de fichiers (telles que la taille du bloc de disque) et du nombre d&#39;entrées de cache. Il est recommandé de réserver deux fois plus d&#39;espace disque pour le cache disque HTTP que la quantité spécifiée par `PS::cache.maxSize`. Un algorithme moins récemment utilisé est utilisé pour maintenir la quantité de données mises en cache dans la limite.

Outre `PS::cache.maxSize`, le cache de réponse est également géré en limitant le nombre maximal d&#39;entrées de cache avec `PS::cache.maxEntries`. Sous Linux, ce paramètre doit spécifier une valeur ne dépassant pas le nombre d&#39;inodes disponibles sur la partition de cache.

>[!NOTE]
>
>Platform Server conserve un index de cache en mémoire. La taille de cet index est de 32 octets multipliée par la valeur de `PS::cache.maxEntries`. Vous devrez peut-être augmenter la taille du tas du serveur de plateformes afin d’accueillir des caches plus grands.

Le système utilise un fichier d&#39;index de cache qui est enregistré sur le disque lorsque le serveur est arrêté de manière ordonnée. En cas de événements inattendus, tels qu&#39;une panne d&#39;alimentation, ce fichier peut ne pas être enregistré. En outre, il peut s’écouler plusieurs minutes avant que le serveur de plateformes ne soit prêt.
