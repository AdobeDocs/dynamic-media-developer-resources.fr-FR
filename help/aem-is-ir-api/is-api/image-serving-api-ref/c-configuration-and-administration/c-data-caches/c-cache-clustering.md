---
description: La mise en grappe du cache permet à plusieurs serveurs à charge équilibrée d'échanger des entrées de cache dans le cache de réponse Principale et le cache de données secondaire (pour les requêtes imbriquées/incorporées), avec le potentiel d'augmenter significativement la réactivité du serveur en éliminant la nécessité de générer la même entrée de cache sur plusieurs serveurs.
solution: Experience Manager
title: Mise en grappe du cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Mise en grappe du cache {#cache-clustering}

La mise en grappe du cache permet à plusieurs serveurs à charge équilibrée d&#39;échanger des entrées de cache dans le cache de réponse Principale et le cache de données secondaire (pour les requêtes imbriquées/incorporées), avec le potentiel d&#39;augmenter significativement la réactivité du serveur en éliminant la nécessité de générer la même entrée de cache sur plusieurs serveurs.

Si ce paramètre est configuré, lorsqu’un serveur reçoit une demande pour un élément qui n’est pas dans le cache local, il contacte les serveurs homologues de la grappe. Il vérifie s’ils possèdent déjà cet élément de données avant de demander au serveur d’images de générer l’élément.

La mise en grappe du cache bénéficie principalement aux applications impliquant des contenus hautement cachetables. Les charges de serveur doivent être considérablement réduites lors du déploiement initial et lors de la mise en service de nouveaux contenus.

Les dépassements de délai et d’autres mesures de protection garantissent que le système continue à fonctionner à pleine capacité même lorsqu’un ou plusieurs serveurs homologues sont hors ligne.

La grappe de cache peut fonctionner dans l’une des deux configurations de base suivantes :

* Lorsque `PS::cacheCluster.updateLocalCache` est activé (par défaut), toute entrée de cache trouvée sur un serveur homologue est copiée dans le cache local.

   Cette configuration réduit le trafic entre les serveurs homologues. Il fournit également les temps de réponse les plus rapides au prix d’une réplication de toutes les entrées de cache sur tous les serveurs de la grappe. Il s’agit de la configuration recommandée.

* Lorsque `PS::cacheCluster.updateLocalCache` est désactivé, les données provenant d&#39;autres serveurs ne sont pas copiées dans le cache local.

   Cela multiplie l’espace disque disponible pour les données de cache. Cependant, il augmente le trafic entre les serveurs homologues et réduit les temps de réponse globaux. Utilisez cette configuration uniquement lorsque vous voyez de faibles taux d’accès au cache.

