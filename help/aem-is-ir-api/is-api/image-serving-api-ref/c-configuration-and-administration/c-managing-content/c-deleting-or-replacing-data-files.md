---
description: Bien que l'ajout de nouveaux fichiers de données soit simple et direct, le remplacement de fichiers de données existants, activement utilisés par le serveur, doit faire l'objet d'une attention particulière. Au lieu de simplement remplacer ces fichiers, il est recommandé de donner un nouveau nom au fichier de remplacement (par exemple, ajouter un suffixe de version au nom du fichier). Une fois le nouveau fichier mis en ligne, l’ancienne version peut être supprimée.
solution: Experience Manager
title: Suppression ou remplacement de fichiers de données
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# Suppression ou remplacement de fichiers de données{#deleting-or-replacing-data-files}

Bien que l&#39;ajout de nouveaux fichiers de données soit simple et direct, le remplacement de fichiers de données existants, activement utilisés par le serveur, doit faire l&#39;objet d&#39;une attention particulière. Au lieu de simplement remplacer ces fichiers, il est recommandé de donner un nouveau nom au fichier de remplacement (par exemple, ajouter un suffixe de version au nom du fichier). Une fois le nouveau fichier mis en ligne, l’ancienne version peut être supprimée.

>[!NOTE]
>
>Les fichiers de données ne doivent jamais être remplacés ou supprimés lors d’une utilisation principale par Image Serving. Des erreurs, voire un blocage du serveur, peuvent se produire autrement.

Dans tous les cas, n&#39;oubliez pas que le cache du serveur de plateformes et les entrées du cache client doivent devenir obsolètes avant que les données mises à jour ne soient visibles par le client. Les entrées de cache spécifiques peuvent être mises à jour immédiatement à l&#39;aide de la commande `cache=validate`.

Les modifications apportées aux fichiers de police et aux fichiers de profil ICC ne sont pas suivies directement par le gestionnaire de cache. Si une telle ressource est modifiée sans modifier son ID, le cache du serveur ne connaît pas la modification et `cache=validate` ne provoque pas la mise à jour de l&#39;entrée du cache. `cache=update` peut être utilisé pour forcer la régénération de ces entrées de cache.

Pour éviter les complications liées au remplacement de fichiers, il est recommandé de donner un nouveau nom à un fichier de remplacement et de mettre à jour les entrées de catalogue correspondantes. Cela permet de remplacer n’importe quel fichier de données pendant que le serveur est actif et de rendre obsolètes les entrées de cache du serveur immédiatement sans intervention supplémentaire. Cette approche peut être utilisée pour les profils ICC, les polices et toutes les images gérées par des catalogues d’images.
