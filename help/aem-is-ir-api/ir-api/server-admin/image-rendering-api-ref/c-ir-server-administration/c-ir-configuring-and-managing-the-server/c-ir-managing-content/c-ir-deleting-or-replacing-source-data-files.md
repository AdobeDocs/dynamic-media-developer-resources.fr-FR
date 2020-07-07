---
description: Les fichiers de vignette peuvent être remplacés ou supprimés pendant que le serveur est actif en utilisant la commande req=release juste avant le remplacement du fichier.
seo-description: Les fichiers de vignette peuvent être remplacés ou supprimés pendant que le serveur est actif en utilisant la commande req=release juste avant le remplacement du fichier.
seo-title: Suppression ou remplacement des fichiers de données source
solution: Experience Manager
title: Suppression ou remplacement des fichiers de données source
topic: Scene7 Image Serving - Image Rendering API
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Suppression ou remplacement des fichiers de données source{#deleting-or-replacing-source-data-files}

Les fichiers de vignette peuvent être remplacés ou supprimés pendant que le serveur est actif en utilisant la commande req=release juste avant le remplacement du fichier.

>[!NOTE]
>
>Un fichier de données ne doit pas être remplacé ou supprimé lorsque le serveur de rendu y accède.

Gardez à l’esprit que la suppression ou le remplacement d’un fichier de données source entraîne uniquement la fermeture du fichier par le serveur de rendu jusqu’à la prochaine demande d’accès à cette vignette. Plusieurs Reprises peuvent être nécessaires si un fichier est fortement utilisé.

Le serveur de rendu doit être arrêté pour remplacer d’autres fichiers de données.

Les entrées du cache de Platform Server sont automatiquement invalidées lorsque des fichiers matières ou des vignettes sont remplacés. Le remplacement des fichiers de profil ICC n’invalide pas les caches.

Pour éviter les complications liées au remplacement de fichiers, il est recommandé de donner un nouveau nom à un fichier de remplacement et de mettre à jour les entrées de catalogue correspondantes. Cela permet de remplacer n’importe quel fichier de données pendant que le serveur est actif et rend les entrées de cache du serveur obsolètes automatiquement sans intervention supplémentaire. Cette approche peut être utilisée pour tous les fichiers de données gérés par des catalogues d’images.
