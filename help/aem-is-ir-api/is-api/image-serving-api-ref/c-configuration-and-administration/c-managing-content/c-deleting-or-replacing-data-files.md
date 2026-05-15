---
description: Bien que l’ajout de nouveaux fichiers de données soit simple et direct, une attention particulière doit être apportée lors du remplacement de fichiers de données existants qui sont utilisés activement par le serveur. Au lieu de remplacer simplement ces fichiers, il est recommandé d’attribuer un nouveau nom au fichier de remplacement (par exemple, d’ajouter un suffixe de version au nom de fichier). Une fois le nouveau fichier activé, l’ancienne version peut être supprimée.
solution: Experience Manager
title: Supprimer ou remplacer des fichiers de données
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
TQID: 'https://experienceleague.adobe.com/RLwRWtyvlbeSlQy4woV6-a-nrq3Sz1q7gviUsTrL2Q4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 322
ht-degree: 0%

---

# Supprimer ou remplacer des fichiers de données{#deleting-or-replacing-data-files}

Bien que l’ajout de nouveaux fichiers de données soit simple et direct, une attention particulière doit être apportée lors du remplacement de fichiers de données existants qui sont utilisés activement par le serveur. Au lieu de remplacer simplement ces fichiers, il est recommandé d’attribuer un nouveau nom au fichier de remplacement (par exemple, d’ajouter un suffixe de version au nom de fichier). Une fois le nouveau fichier activé, l’ancienne version peut être supprimée.

>[!NOTE]
>
>Les fichiers de données ne doivent jamais être remplacés ou supprimés lorsqu’ils sont utilisés activement par le service d’images. Des erreurs, voire un blocage du serveur, peuvent se produire dans le cas contraire.

Dans tous les cas, souvenez-vous que le cache [!DNL Platform Server] et les entrées du cache client doivent devenir obsolètes avant que les données mises à jour ne soient visibles par le client. Les entrées de cache spécifiques peuvent être mises à jour immédiatement à l’aide de la commande `cache=validate`.

Les modifications apportées aux fichiers de polices et aux fichiers de profil ICC ne sont pas suivies directement par le gestionnaire de cache. Si une telle ressource est modifiée sans modifier son identifiant, le cache du serveur n’est pas informé de la modification et `cache=validate` n’entraîne pas la mise à jour de l’entrée du cache. `cache=update` peut être utilisé pour forcer la régénération de ces entrées de cache.

Pour éviter les complications du remplacement des fichiers, il est recommandé d’attribuer un nouveau nom à un fichier de remplacement et de mettre à jour les entrées de catalogue correspondantes. Cela permet de remplacer n’importe quel fichier de données lorsque le serveur est actif et rend les entrées du cache du serveur immédiatement obsolètes, sans intervention supplémentaire. Cette approche peut être utilisée pour les profils ICC, les polices et toutes les images gérées par les catalogues d’images.
