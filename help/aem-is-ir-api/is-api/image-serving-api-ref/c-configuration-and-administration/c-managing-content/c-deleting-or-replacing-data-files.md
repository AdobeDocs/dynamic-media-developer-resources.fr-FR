---
description: Bien que l’ajout de nouveaux fichiers de données soit simple et direct, il faut prendre soin de remplacer les fichiers de données existants qui sont activement utilisés par le serveur. Au lieu de simplement remplacer ces fichiers, il est recommandé de donner un nouveau nom au fichier de remplacement (par exemple, ajouter un suffixe de version au nom du fichier). Une fois le nouveau fichier mis en ligne, l’ancienne version peut être supprimée.
seo-description: Bien que l’ajout de nouveaux fichiers de données soit simple et direct, il faut prendre soin de remplacer les fichiers de données existants qui sont activement utilisés par le serveur. Au lieu de simplement remplacer ces fichiers, il est recommandé de donner un nouveau nom au fichier de remplacement (par exemple, ajouter un suffixe de version au nom du fichier). Une fois le nouveau fichier mis en ligne, l’ancienne version peut être supprimée.
seo-title: Suppression ou remplacement de fichiers de données
solution: Experience Manager
title: Suppression ou remplacement de fichiers de données
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b446144-48f6-4b50-93ec-0287425d932a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Suppression ou remplacement de fichiers de données{#deleting-or-replacing-data-files}

Bien que l’ajout de nouveaux fichiers de données soit simple et direct, il faut prendre soin de remplacer les fichiers de données existants qui sont activement utilisés par le serveur. Au lieu de simplement remplacer ces fichiers, il est recommandé de donner un nouveau nom au fichier de remplacement (par exemple, ajouter un suffixe de version au nom du fichier). Une fois le nouveau fichier mis en ligne, l’ancienne version peut être supprimée.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Les fichiers de données ne doivent jamais être remplacés ou supprimés lors d’une utilisation active par Image Serving. Des erreurs, voire un blocage du serveur, peuvent se produire autrement.

Dans tous les cas, n’oubliez pas que le cache du serveur de plateformes et les entrées du cache client doivent devenir obsolètes avant que les données mises à jour ne soient affichées par le client. Les entrées de cache spécifiques peuvent être mises à jour immédiatement à l’aide de la `cache=validate` commande.

Les modifications apportées aux fichiers de police et aux fichiers de ICC ne sont pas suivies directement par le gestionnaire de cache. Si une telle ressource est modifiée sans modifier son ID, le cache du serveur ne connaîtra pas la modification et ne `cache=validate` provoquera pas la mise à jour de l’entrée du cache. `cache=update` peut être utilisé pour forcer la régénération de ces entrées de cache.

Afin d’éviter les complications liées au remplacement de fichiers, il est recommandé de donner un nouveau nom à un fichier de remplacement et de mettre à jour les entrées correspondantes du catalogue. Cela permet de remplacer tout fichier de données pendant que le serveur est en ligne et de rendre les entrées du cache du serveur obsolètes immédiatement sans intervention supplémentaire. Cette approche peut être utilisée pour les  ICC, les polices et toutes les images gérées par des catalogues d’images.
