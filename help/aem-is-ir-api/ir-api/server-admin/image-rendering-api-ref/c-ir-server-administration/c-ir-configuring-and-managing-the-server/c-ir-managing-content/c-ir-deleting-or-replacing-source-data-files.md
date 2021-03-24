---
description: Les fichiers de vignette peuvent être remplacés ou supprimés pendant que le serveur est actif en utilisant la commande req=release juste avant le remplacement du fichier.
solution: Experience Manager
title: Suppression ou remplacement des fichiers de données source
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Suppression ou remplacement des fichiers de données source{#deleting-or-replacing-source-data-files}

Les fichiers de vignette peuvent être remplacés ou supprimés pendant que le serveur est actif en utilisant la commande req=release juste avant le remplacement du fichier.

>[!NOTE]
>
>Un fichier de données ne doit pas être remplacé ou supprimé lorsque le serveur de rendu y accède.

Gardez à l’esprit que la suppression ou le remplacement d’un fichier de données source entraîne uniquement la fermeture du fichier par le serveur de rendu jusqu’à la prochaine demande d’accès à cette vignette. Plusieurs Reprises peuvent être nécessaires si un fichier est fortement utilisé.

Le serveur de rendu doit être arrêté pour remplacer d’autres fichiers de données.

Les entrées de cache du serveur de plateformes sont automatiquement invalidées lorsque des fichiers de matières ou des vignettes sont remplacés. Le remplacement des fichiers de profil ICC n’invalide pas les caches.

Pour éviter les complications liées au remplacement de fichiers, il est recommandé de donner un nouveau nom à un fichier de remplacement et de mettre à jour les entrées de catalogue correspondantes. Cela permet de remplacer n’importe quel fichier de données pendant que le serveur est actif et rend les entrées de cache du serveur obsolètes automatiquement sans intervention supplémentaire. Cette approche peut être utilisée pour tous les fichiers de données gérés par des catalogues d’images.
