---
description: Les serveurs IS peuvent être configurés pour basculer vers d’autres serveurs pour les demandes qui impliquent une image source qui ne peut pas être ouverte ou lue correctement.
solution: Experience Manager
title: Redirection en cas d’erreur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Redirection en cas d’erreur{#redirect-on-error}

Les serveurs IS peuvent être configurés pour basculer vers d’autres serveurs pour les demandes qui impliquent une image source qui ne peut pas être ouverte ou lue correctement.

Les types de demandes suivants sont redirigés :

* Image IS Images figurant dans le catalogue, mais pas sur le disque.

  Si une image ne figure pas dans un catalogue, la redirection de l’erreur ne doit pas se produire lorsque l’image est introuvable.

* Images, profils de couleurs ou polices corrompus.
* Le contenu statique est introuvable sur le disque.

  Les demandes de contenu statique sont redirigées lorsqu’il est introuvable sur le disque, même si le contenu statique référencé n’a pas d’enregistrement de catalogue.

L’erreur de redirection ne se produit dans aucun autre cas.

Lorsque cette option est activée et lorsqu’une telle erreur se produit pendant le traitement de la demande, le serveur primaire envoie la demande au serveur secondaire pour traitement. La réponse, qu’elle indique un succès ou un échec, est ensuite transmise directement au client. Le serveur principal marque les entrées de journal de ces demandes transférées avec l’utilisation `REMOTE`du cache. Les données de réponse ne sont pas mises en cache localement par le serveur primaire.

La redirection d’erreur est activée en définissant `PS::errorRedirect.rootUrl` le nom de domaine HTTP et le numéro de port du serveur secondaire. En outre, le délai d’expiration de connexion est configuré avec `PS::errorRedirect.connectTimeout` et la durée maximale pendant laquelle le serveur primaire attend une réponse du serveur secondaire avant de renvoyer une erreur au client est configurée avec `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Si le serveur secondaire ne peut pas être contacté, une réponse d’erreur textuelle est renvoyée au client, même si une image par défaut ou une image d’erreur est configurée.

>[!NOTE]
>
>Les barres verticales (|) du chemin d’accès réseau ne sont pas prises en charge pour la redirection d’erreur.

## Voir aussi {#section-2e8bfc128b944baf8108279d16492f3f}

[Redirection d’erreur](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
