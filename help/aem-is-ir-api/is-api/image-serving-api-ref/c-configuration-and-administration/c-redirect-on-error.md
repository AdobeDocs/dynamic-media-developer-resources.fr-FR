---
description: Les serveurs IS peuvent être configurés pour basculer vers d'autres serveurs pour les requêtes impliquant une image source qui ne peut pas être ouverte ou lue correctement.
solution: Experience Manager
title: Redirection en cas d’erreur
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# Redirection en cas d&#39;erreur{#redirect-on-error}

Les serveurs IS peuvent être configurés pour basculer vers d&#39;autres serveurs pour les requêtes impliquant une image source qui ne peut pas être ouverte ou lue correctement.

Les types de demandes suivants sont redirigés :

* IS Images qui se trouvent dans le catalogue, mais pas sur le disque.

   Si une image ne figure pas dans un catalogue, une erreur de redirection ne doit pas se produire lorsque l’image est introuvable.

* Images, profils de couleur ou polices corrompus.
* Contenu statique introuvable sur le disque.

   Les requêtes de contenu statique sont redirigées lorsqu’elles sont introuvables sur le disque, même si le contenu statique référencé ne comporte pas d’enregistrement de catalogue.

La redirection d’erreur ne se produira dans aucun autre cas.

Lorsqu&#39;elle est activée et qu&#39;une telle erreur survient pendant le traitement de la requête, le serveur Principal envoie la requête au serveur secondaire pour traitement. La réponse, qu’elle indique un succès ou un échec, est ensuite transmise directement au client. Le serveur Principal marque les entrées du journal de ces requêtes transférées avec l&#39;utilisation du cache `REMOTE`. Les données de réponse ne sont pas mises en cache localement par le serveur Principal.

La redirection d&#39;erreur est activée en définissant `PS::errorRedirect.rootUrl` sur le nom de domaine HTTP et le numéro de port du serveur secondaire. En outre, le délai d’expiration de la connexion est configuré avec `PS::errorRedirect.connectTimeout` et le délai maximal pendant lequel le serveur Principal attend une réponse du serveur secondaire avant de renvoyer une erreur au client est configuré avec `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Si le serveur secondaire ne peut pas être contacté, une réponse d’erreur texte est renvoyée au client, même si une image par défaut ou une image d’erreur est configurée.

>[!NOTE]
>
>Les caractères (|) du chemin d’accès réseau ne sont pas pris en charge pour la redirection d’erreur.

## Voir aussi {#section-2e8bfc128b944baf8108279d16492f3f}

[Redirection d&#39;erreur](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
