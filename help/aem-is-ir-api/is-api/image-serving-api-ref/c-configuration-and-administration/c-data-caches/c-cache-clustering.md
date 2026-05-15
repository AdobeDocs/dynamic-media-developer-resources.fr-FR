---
description: Le clustering du cache permet à plusieurs serveurs à charge équilibrée d’échanger des entrées de cache dans le cache de réponse principal et le cache de données secondaire (pour les requêtes imbriquées/intégrées), avec la possibilité d’augmenter considérablement la réactivité du serveur en éliminant la nécessité de générer la même entrée de cache sur plusieurs serveurs.
solution: Experience Manager
title: Mise en cluster du cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
TQID: 'https://experienceleague.adobe.com/J1QtNEy9i67oveb1oS2V6-fagqrrlC30oih8AS1g-N4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 0%

---

# Mise en cluster du cache{#cache-clustering}

Le clustering du cache permet à plusieurs serveurs à charge équilibrée d’échanger des entrées de cache dans le cache de réponse principal et le cache de données secondaire (pour les requêtes imbriquées/intégrées), avec la possibilité d’augmenter considérablement la réactivité du serveur en éliminant la nécessité de générer la même entrée de cache sur plusieurs serveurs.

Si tel est le cas, lorsqu’un serveur reçoit une demande pour un élément qui n’est pas dans le cache local, il contacte les serveurs homologues du cluster. Il vérifie s’ils disposent déjà de cet élément de données avant de demander au serveur d’images de générer l’élément.

La mise en cluster du cache bénéficie principalement aux applications impliquant des contenus hautement susceptibles d’être mis en cache. Les charges du serveur doivent être réduites de manière significative lors du déploiement initial et de la mise en ligne avec de nouveaux contenus.

Les délais d’expiration et d’autres mesures de protection garantissent que le système continue à fonctionner à pleine capacité même lorsqu’un ou plusieurs serveurs homologues sont hors ligne.

Le cluster de cache peut fonctionner dans l’une des deux configurations de base suivantes :

* Lorsque `PS::cacheCluster.updateLocalCache` est activé (par défaut), toute entrée de cache trouvée sur un serveur homologue est copiée dans le cache local.

  Cette configuration réduit le trafic entre les serveurs d’homologues. Il offre également les temps de réponse les plus rapides, au prix de la réplication de toutes les entrées de cache vers tous les serveurs du cluster. Il s’agit de la configuration recommandée.

* Lorsque `PS::cacheCluster.updateLocalCache` est désactivé, les données des autres serveurs ne sont pas copiées dans le cache local.

  L’espace disque disponible pour les données du cache est ainsi multiplié. Toutefois, cela augmente le trafic entre les serveurs d’homologues et réduit les temps de réponse globaux. Utilisez cette configuration uniquement lorsque les taux d’accès au cache sont faibles.
