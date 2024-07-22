---
description: La mise en grappe du cache permet à plusieurs serveurs à charge équilibrée d’exchange des entrées de cache dans le cache de réponse principal et le cache de données secondaire (pour les requêtes imbriquées/incorporées), avec le potentiel d’augmenter considérablement la réactivité du serveur en éliminant la nécessité de générer la même entrée de cache sur plusieurs serveurs.
solution: Experience Manager
title: Mise en grappe du cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Mise en grappe du cache{#cache-clustering}

La mise en grappe du cache permet à plusieurs serveurs à charge équilibrée d’exchange des entrées de cache dans le cache de réponse principal et le cache de données secondaire (pour les requêtes imbriquées/incorporées), avec le potentiel d’augmenter considérablement la réactivité du serveur en éliminant la nécessité de générer la même entrée de cache sur plusieurs serveurs.

Si cette configuration est activée, lorsqu’un serveur reçoit une demande pour un élément qui n’est pas dans le cache local, il contacte les serveurs pairs de la grappe. Il vérifie s’ils disposent déjà de cet élément de données avant de demander au serveur d’images de générer l’élément.

La mise en grappe du cache avantage principalement les applications impliquant des contenus hautement mis en cache. Les chargements du serveur doivent être considérablement réduits lors du déploiement initial et lors de la mise en ligne de nouveaux contenus.

Les dépassements de délai et autres protections garantissent que le système continue à fonctionner à pleine capacité même lorsqu’un ou plusieurs des serveurs pairs sont hors ligne.

La grappe de cache peut fonctionner dans l’une des deux configurations de base suivantes :

* Lorsque `PS::cacheCluster.updateLocalCache` est activé (par défaut), toute entrée de cache trouvée sur un serveur homologue est copiée dans le cache local.

  Cette configuration réduit le trafic entre les serveurs pairs. Il fournit également les temps de réponse les plus rapides au prix de la réplication de toutes les entrées de cache sur tous les serveurs de la grappe. Il s’agit de la configuration recommandée.

* Lorsque `PS::cacheCluster.updateLocalCache` est désactivé, les données des autres serveurs ne sont pas copiées dans le cache local.

  Cela multiplie l’espace disque disponible pour les données de cache. Cependant, cela augmente le trafic entre les serveurs pairs et réduit les temps de réponse globaux. Utilisez cette configuration uniquement lorsque les taux d’accès au cache sont faibles.
