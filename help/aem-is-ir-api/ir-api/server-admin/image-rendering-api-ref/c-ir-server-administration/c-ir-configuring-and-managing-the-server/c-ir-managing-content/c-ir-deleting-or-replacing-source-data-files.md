---
description: Les fichiers de vignette peuvent être remplacés ou supprimés pendant que le serveur est en ligne à l’aide de la commande req=release juste avant le remplacement du fichier.
seo-description: Les fichiers de vignette peuvent être remplacés ou supprimés pendant que le serveur est en ligne à l’aide de la commande req=release juste avant le remplacement du fichier.
seo-title: Suppression ou remplacement des fichiers de données source
solution: Experience Manager
title: Suppression ou remplacement des fichiers de données source
topic: Scene7 Image Serving - Image Rendering API
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Suppression ou remplacement des fichiers de données source{#deleting-or-replacing-source-data-files}

Les fichiers de vignette peuvent être remplacés ou supprimés pendant que le serveur est en ligne à l’aide de la commande req=release juste avant le remplacement du fichier.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Un fichier de données ne doit pas être remplacé ni supprimé lorsque le serveur de rendu y accède.

N’oubliez pas que la suppression ou le remplacement d’un fichier de données source entraîne uniquement la fermeture du fichier par le serveur de rendu jusqu’à la prochaine requête qui accède à cette vignette. Plusieurs  peuvent être nécessaires si un fichier est fortement utilisé.

Le serveur de rendu doit être arrêté pour remplacer d’autres fichiers de données.

Les entrées du cache du serveur de plateformes sont automatiquement invalidées lorsque les fichiers matières ou les vignettes sont remplacés. Le remplacement des fichiers  ICC n’invalide pas les caches.

Afin d’éviter les complications liées au remplacement de fichiers, il est recommandé de donner un nouveau nom à un fichier de remplacement et de mettre à jour les entrées correspondantes du catalogue. Cela permet de remplacer tout fichier de données pendant que le serveur est actif et rend les entrées du cache du serveur obsolètes automatiquement sans intervention supplémentaire. Cette approche peut être utilisée pour tous les fichiers de données gérés par des catalogues d’images.
