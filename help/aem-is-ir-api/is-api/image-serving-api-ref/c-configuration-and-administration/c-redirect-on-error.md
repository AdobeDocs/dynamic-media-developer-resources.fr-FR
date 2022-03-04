---
description: Les serveurs IS peuvent être configurés pour basculer vers d’autres serveurs pour les demandes impliquant une image source qui ne peut pas être ouverte ni lue correctement.
solution: Experience Manager
title: Redirection en erreur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# Redirection en erreur{#redirect-on-error}

Les serveurs IS peuvent être configurés pour basculer vers d’autres serveurs pour les demandes impliquant une image source qui ne peut pas être ouverte ni lue correctement.

Les types de requêtes suivants sont redirigés :

* IS Images qui se trouvent dans le catalogue, mais pas sur le disque.

   Si une image ne figure pas dans un catalogue, une erreur de redirection ne doit pas se produire lorsque l’image est introuvable.

* Images, profils de couleurs ou polices corrompus.
* Le contenu statique est introuvable sur le disque.

   Les demandes de contenu statique sont redirigées lorsqu’elles sont introuvables sur le disque, même si le contenu statique référencé ne comporte pas d’enregistrement de catalogue.

La redirection d’erreur ne se produira dans aucun autre cas.

Lorsqu’elle est activée et qu’une telle erreur se produit pendant le traitement de la demande, le serveur Principal envoie la demande au serveur secondaire pour traitement. La réponse, qu’elle indique un succès ou un échec, est ensuite transmise directement au client. Le serveur Principal marque les entrées de journal de ces requêtes transférées avec l’utilisation du cache `REMOTE`. Les données de réponse ne sont pas mises en cache localement par le serveur Principal.

La redirection d’erreur est activée en définissant `PS::errorRedirect.rootUrl` au nom de domaine HTTP et au numéro de port du serveur secondaire. En outre, le délai de connexion est configuré avec `PS::errorRedirect.connectTimeout` et la durée maximale pendant laquelle le serveur Principal attend une réponse du serveur secondaire avant de renvoyer une erreur au client est configuré avec `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Si le serveur secondaire ne peut pas être contacté, une réponse d’erreur texte est renvoyée au client, même si une image par défaut ou une image d’erreur est configurée.

>[!NOTE]
>
>Les caractères de pixel (|) dans le chemin d’accès net ne sont pas pris en charge pour la redirection d’erreur.

## Voir aussi {#section-2e8bfc128b944baf8108279d16492f3f}

[Redirection des erreurs](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
