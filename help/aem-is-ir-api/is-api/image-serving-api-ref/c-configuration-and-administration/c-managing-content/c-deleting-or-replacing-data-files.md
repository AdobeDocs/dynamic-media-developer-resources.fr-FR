---
description: Bien que l’ajout de nouveaux fichiers de données soit simple et direct, des précautions particulières doivent être prises lors du remplacement des fichiers de données existants qui sont activement utilisés par le serveur. Au lieu de simplement remplacer ces fichiers, il est recommandé de donner un nouveau nom au fichier de remplacement (par exemple, ajouter un suffixe de version au nom de fichier). Une fois le nouveau fichier mis en ligne, l’ancienne version peut être supprimée.
solution: Experience Manager
title: Suppression ou remplacement des fichiers de données
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Suppression ou remplacement des fichiers de données{#deleting-or-replacing-data-files}

Bien que l’ajout de nouveaux fichiers de données soit simple et direct, des précautions particulières doivent être prises lors du remplacement des fichiers de données existants qui sont activement utilisés par le serveur. Au lieu de simplement remplacer ces fichiers, il est recommandé de donner un nouveau nom au fichier de remplacement (par exemple, ajouter un suffixe de version au nom de fichier). Une fois le nouveau fichier mis en ligne, l’ancienne version peut être supprimée.

>[!NOTE]
>
>Les fichiers de données ne doivent jamais être remplacés ou supprimés lorsqu’ils sont utilisés activement par Image Server. Des erreurs ou même une panne de serveur peuvent se produire autrement.

Dans tous les cas, n’oubliez pas que le [!DNL Platform Server] cache et les entrées de cache client doivent devenir obsolètes avant que les données mises à jour ne soient vues par le client. Les entrées de cache spécifiques peuvent être mises à jour immédiatement à l’aide de la `cache=validate` commande.

Les modifications apportées aux fichiers de polices et aux fichiers de profil ICC ne sont pas suivies directement par le gestionnaire de cache. Si une telle ressource est modifiée sans modifier son ID, le cache du serveur n’est pas informé de la modification et `cache=validate` n’entraîne pas la mise à jour de l’entrée de cache. `cache=update` peut être utilisé pour forcer la régénération de ces entrées de cache.

Pour éviter les complications liées au remplacement des fichiers, il est recommandé de donner un nouveau nom à un fichier de remplacement et de mettre à jour les entrées de catalogue correspondantes. Cela permet de remplacer n’importe quel fichier de données pendant que le serveur est actif et de rendre les entrées de cache du serveur immédiatement obsolètes sans intervention supplémentaire. Cette approche peut être utilisée pour les profils ICC, les polices et toutes les images gérées par les catalogues d’images.
