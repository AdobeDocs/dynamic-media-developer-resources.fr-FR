---
description: Le serveur de plateformes met en cache toutes les images de réponse et certaines données texte sur le disque, sauf si une requête est marquée comme non pouvant être mise en cache.
seo-description: Le serveur de plateformes met en cache toutes les images de réponse et certaines données texte sur le disque, sauf si une requête est marquée comme non pouvant être mise en cache.
seo-title: Cache de données de réponse
solution: Experience Manager
title: Cache de données de réponse
topic: Scene7 Image Serving - Image Rendering API
uuid: dbfda210-3b50-4e8c-8d77-7263ae4e80a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Cache de données de réponse{#response-data-cache}

Le serveur de plateformes met en cache toutes les images de réponse et certaines données texte sur le disque, sauf si une requête est marquée comme non pouvant être mise en cache.

L’emplacement du cache disque du serveur de plateformes est défini avec `PS::cache.rootPaths`.

Pour les applications qui présentent un taux d’accès élevé au cache, vous pouvez augmenter les performances et la capacité du serveur en répartissant le cache de données de réponse entre plusieurs périphériques de disque. Pour ce faire, créez un dossier racine de cache sur chaque disque et enregistrez-le dans `PS::cache.rootPaths`.

`PS::cache.maxSize` indique la taille totale de toutes les entrées de cache, sans tenir compte de la surcharge du système de fichiers. La quantité d&#39;espace disque réellement requise dépend des propriétés du système de fichiers, telles que la taille du bloc de disque, et du nombre d&#39;entrées de cache. Il est recommandé de réserver deux fois plus d&#39;espace disque pour le cache disque HTTP que la quantité spécifiée par `PS::cache.maxSize`. Un algorithme utilisé le moins récemment est utilisé pour maintenir la quantité de données mises en cache dans la limite.

En outre, `PS::cache.maxSize`le cache de réponses est également géré en limitant le nombre maximal d’entrées de cache avec `PS::cache.maxEntries`. Sous Linux, ce paramètre doit spécifier une valeur ne dépassant pas le nombre d’inodes disponibles sur la partition cache.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Le serveur de plateformes conserve un index de cache en mémoire. La taille de cet index est de 32 octets par rapport à la valeur de `PS::cache.maxEntries`. Vous devrez peut-être augmenter la taille du tas du serveur de plateformes afin d’accueillir des caches plus grands.

Le système utilise un fichier d’index de cache qui est enregistré sur le disque lorsque le serveur est arrêté de manière ordonnée. En cas de  inattendu, comme une panne d&#39;alimentation, ce fichier peut ne pas être enregistré. En outre, il peut s’écouler plusieurs minutes avant que le serveur de plateformes ne soit prêt.
