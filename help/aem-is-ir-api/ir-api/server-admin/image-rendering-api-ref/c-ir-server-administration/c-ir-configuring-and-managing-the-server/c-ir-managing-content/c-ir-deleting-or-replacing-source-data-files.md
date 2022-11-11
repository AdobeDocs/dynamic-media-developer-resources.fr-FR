---
description: Les fichiers de vignette peuvent être remplacés ou supprimés pendant que le serveur est en ligne en utilisant la commande req=release juste avant le remplacement du fichier.
solution: Experience Manager
title: Suppression ou remplacement des fichiers de données sources
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Suppression ou remplacement des fichiers de données sources{#deleting-or-replacing-source-data-files}

Les fichiers de vignette peuvent être remplacés ou supprimés pendant que le serveur est en ligne en utilisant la commande req=release juste avant le remplacement du fichier.

>[!NOTE]
>
>Un fichier de données ne doit pas être remplacé ni supprimé lorsque le serveur de rendu y accède.

Gardez à l’esprit que la suppression ou le remplacement d’un fichier de données source entraîne uniquement le serveur de rendu à fermer le fichier jusqu’à la requête suivante qui accède à cette vignette. Plusieurs reprises peuvent être nécessaires si un fichier est fortement utilisé.

Le serveur de rendu doit être arrêté pour remplacer d’autres fichiers de données.

[!DNL Platform Server] les entrées de cache sont automatiquement invalidées lorsque les fichiers de matériaux ou les vignettes sont remplacés. Le remplacement des fichiers de profil ICC n’invalide pas les caches.

Pour éviter toute difficulté liée au remplacement de fichiers, il est recommandé de donner un nouveau nom à un fichier de remplacement et de mettre à jour les entrées de catalogue correspondantes. Cela permet de remplacer n’importe quel fichier de données pendant que le serveur est en ligne et entraîne l’obsolescence automatique des entrées de cache du serveur sans intervention supplémentaire. Cette approche peut être utilisée pour tous les fichiers de données gérés par les catalogues d’images.
