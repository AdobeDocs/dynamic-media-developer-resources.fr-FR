---
description: Les serveurs IMS peuvent être configurés pour basculer vers d’autres serveurs pour les demandes impliquant une image source qui ne peut pas être ouverte ou lue correctement.
solution: Experience Manager
title: Rediriger en cas d’erreur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
TQID: 'https://experienceleague.adobe.com/jNvJP4nJ7W1thf-ZDbSCzry54H8wI4DVGK8FW6koNCw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 0%

---

# Rediriger en cas d’erreur{#redirect-on-error}

Les serveurs IMS peuvent être configurés pour basculer vers d’autres serveurs pour les demandes impliquant une image source qui ne peut pas être ouverte ou lue correctement.

Les types de requêtes suivants sont redirigés :

* Images IS qui se trouvent dans le catalogue, mais pas sur le disque.

  Si une image ne figure pas dans un catalogue, la redirection d’erreur ne doit pas se produire lorsque l’image est introuvable.

* Images, profils de couleurs ou polices corrompus.
* Le contenu statique est introuvable sur le disque.

  Les demandes de contenu statique sont redirigées lorsqu’elles sont introuvables sur le disque, même si le contenu statique référencé ne dispose pas d’un enregistrement de catalogue.

La redirection d’erreur ne se produit dans aucun autre cas.

Lorsqu’elle est activée et qu’une telle erreur se produit lors du traitement de la requête, le serveur principal envoie la requête au serveur secondaire pour traitement. La réponse, qu’elle indique la réussite ou l’échec, est ensuite transférée directement au client. Le serveur principal marque les entrées de journal de ces requêtes transférées avec des `REMOTE` d’utilisation du cache. Les données de réponse ne sont pas mises en cache localement par le serveur principal.

La redirection d’erreur est activée en définissant `PS::errorRedirect.rootUrl` sur le nom de domaine HTTP et le numéro de port du serveur secondaire. En outre, le délai d’expiration de la connexion est configuré avec `PS::errorRedirect.connectTimeout` et le temps maximal pendant lequel le serveur principal attend une réponse du serveur secondaire avant de renvoyer une erreur au client est configuré avec `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Si le serveur secondaire ne peut pas être contacté, une réponse d’erreur de texte est renvoyée au client, même si une image par défaut ou une image d’erreur est configurée.

>[!NOTE]
>
>Les caractères de barre verticale (|) du chemin suivant ne sont pas pris en charge pour la redirection des erreurs.

## Voir aussi {#section-2e8bfc128b944baf8108279d16492f3f}

[Redirection d’erreur](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
