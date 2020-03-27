---
description: La mise en grappe du cache permet à plusieurs serveurs à charge équilibrée d’échanger des entrées de cache dans le cache de réponse principal et le cache de données secondaire (pour les requêtes imbriquées/incorporées), avec le potentiel d'augmenter significativement la réactivité du serveur en éliminant la nécessité de générer la même entrée de cache sur plusieurs serveurs.
seo-description: La mise en grappe du cache permet à plusieurs serveurs à charge équilibrée d’échanger des entrées de cache dans le cache de réponse principal et le cache de données secondaire (pour les requêtes imbriquées/incorporées), avec le potentiel d'augmenter significativement la réactivité du serveur en éliminant la nécessité de générer la même entrée de cache sur plusieurs serveurs.
seo-title: Mise en grappe du cache
solution: Experience Manager
title: Mise en grappe du cache
topic: Scene7 Image Serving - Image Rendering API
uuid: 347165d6-a9e7-406e-81a8-8a91f745ce27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Mise en grappe du cache{#cache-clustering}

La mise en grappe du cache permet à plusieurs serveurs à charge équilibrée d’échanger des entrées de cache dans le cache de réponse principal et le cache de données secondaire (pour les requêtes imbriquées/incorporées), avec le potentiel d&#39;augmenter significativement la réactivité du serveur en éliminant la nécessité de générer la même entrée de cache sur plusieurs serveurs.

Si cette configuration est effectuée, lorsqu’un serveur reçoit une demande pour un élément qui n’est pas dans le cache local, il contacte les serveurs homologues de la grappe. Il vérifie s’ils possèdent déjà cet élément de données avant de demander au serveur d’images de générer l’élément.

La mise en grappe du cache bénéficie principalement aux applications impliquant des contenus à haut niveau de mise en cache. Les charges de serveur doivent être considérablement réduites lors du déploiement initial et lors de la mise en service de nouveaux contenus.

Les dépassements de délai et d’autres mesures de protection garantissent que le système continue à fonctionner à pleine capacité, même lorsqu’un ou plusieurs des serveurs homologues sont hors ligne.

La grappe de cache peut fonctionner dans l’une des deux configurations de base suivantes :

* Lorsque `PS::cacheCluster.updateLocalCache` est activé (par défaut), toute entrée de cache trouvée sur un serveur homologue est copiée dans le cache local.

   Cette configuration réduit le trafic entre les serveurs homologues. Il offre également les temps de réponse les plus rapides au coût de la réplication de toutes les entrées de cache sur tous les serveurs de la grappe. Il s’agit de la configuration recommandée.

* Lorsque `PS::cacheCluster.updateLocalCache` est désactivé, les données d’autres serveurs ne sont pas copiées dans le cache local.

   Cela multiplie l’espace disque disponible pour les données de cache. Cependant, il augmente le trafic entre les serveurs homologues et réduit les temps de réponse globaux. Utilisez cette configuration uniquement lorsque vous constatez des taux d’accès au cache faibles.

