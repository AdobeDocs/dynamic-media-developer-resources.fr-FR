---
description: Bien que l’ajout de nouveaux fichiers de données soit simple et direct, le remplacement de fichiers de données existants, activement utilisés par le serveur, doit faire l’objet d’une attention particulière. Au lieu de simplement remplacer ces fichiers, il est recommandé de donner au fichier de remplacement un nouveau nom (par exemple, ajouter un suffixe de version au nom du fichier). Une fois le nouveau fichier mis en ligne, l’ancienne version peut être supprimée.
solution: Experience Manager
title: Suppression ou remplacement de fichiers de données
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Suppression ou remplacement de fichiers de données{#deleting-or-replacing-data-files}

Bien que l’ajout de nouveaux fichiers de données soit simple et direct, le remplacement de fichiers de données existants, activement utilisés par le serveur, doit faire l’objet d’une attention particulière. Au lieu de simplement remplacer ces fichiers, il est recommandé de donner au fichier de remplacement un nouveau nom (par exemple, ajouter un suffixe de version au nom du fichier). Une fois le nouveau fichier mis en ligne, l’ancienne version peut être supprimée.

>[!NOTE]
>
>Les fichiers de données ne doivent jamais être remplacés ou supprimés lors d’une utilisation principale par le serveur d’images. Des erreurs, voire un blocage du serveur, peuvent se produire dans le cas contraire.

Dans tous les cas, n’oubliez pas que le cache du serveur de plateforme et les entrées du cache client doivent devenir obsolètes avant que le client ne voie les données mises à jour. Des entrées de cache spécifiques peuvent être mises à jour immédiatement à l’aide de la commande `cache=validate`.

Les modifications apportées aux fichiers de polices et de profil ICC ne sont pas suivies directement par le gestionnaire de cache. Si une telle ressource est modifiée sans modifier son identifiant, le cache du serveur ne sera pas informé de la modification et `cache=validate` ne provoquera pas la mise à jour de l’entrée du cache. `cache=update` peut être utilisé pour forcer la régénération de ces entrées de cache.

Pour éviter toute difficulté liée au remplacement de fichiers, il est recommandé de donner un nouveau nom à un fichier de remplacement et de mettre à jour les entrées de catalogue correspondantes. Cela permet de remplacer n’importe quel fichier de données pendant que le serveur est en ligne et entraîne l’obsolescence immédiate des entrées du cache du serveur sans intervention supplémentaire. Cette approche peut être utilisée pour les profils ICC, les polices et toutes les images gérées par les catalogues d’images.
