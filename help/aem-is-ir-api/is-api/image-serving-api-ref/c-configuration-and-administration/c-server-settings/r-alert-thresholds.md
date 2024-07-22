---
description: Utilisez ces paramètres de serveur pour configurer les seuils d’alerte.
solution: Experience Manager
title: Seuils d'alerte
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Seuils d&#39;alerte{#alert-thresholds}

Utilisez ces paramètres de serveur pour configurer les seuils d’alerte.

## AS: monitorAlertGenerator.maxAverageResponseTime -Response Time-Seuil de temps de réponseAS: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

Une alerte de temps de réponse est émise lorsque la durée moyenne de traitement d’une requête au cours de l’intervalle d’échantillonnage dépasse le seuil défini ici. Exprimé en msec ; entier 0 ou plus. Les valeurs types sont comprises entre 100 et 1 000 ms, selon la complexité des opérations.

>[!NOTE]
>
>Les requêtes qui génèrent un état de réponse 4xx ou 5xx ne sont pas prises en compte pour cette alerte.

## AS::monitorAlertGenerator.maxErrorRate - Error Response Rate SeuholdAS::monitorAlertGenerator.maxErrorRate - Error Response Rate {#section-76ba77fd3102419395e0f86719a1f3ec}

Une alerte d’erreur est émise lorsque le rapport entre les réponses d’erreur HTTP et le nombre total de réponses durant l’intervalle d’échantillonnage dépasse le seuil spécifié.

Valeur réelle comprise entre 0,0 et 1,0. Généralement définie sur entre 0,005 et 0,1. Définissez cette variable sur 1 pour désactiver les alertes d’erreur.

## AS::monitorAlertGenerator.minRequestRate - Faible seuil de trafic {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Une alerte de trafic minimale est envoyée lorsque le nombre moyen de demandes reçues par seconde au cours de l’intervalle d’échantillonnage actuel est inférieur à ce seuil. Désactivez l’alerte en définissant cette valeur sur 0. Exprimé dans les requêtes par seconde. Valeur réelle 0 ou supérieure.

## AS::monitorAlertGenerator.minFreeHeapSpace - Seuil d’espace-tas libre {#section-ce6705045f6842769030ccb1894594cc}

Spécifie l’espace de tas Java libre minimum. Une alerte de priorité est envoyée immédiatement après un cycle de nettoyage de la mémoire Java lorsque l’espace de tas disponible est inférieur à ce seuil. 50 Mo est recommandé pour un fonctionnement sécurisé de [!DNL Platform Server]. Le fait de conserver un espace de tas libre au-dessus de cette valeur réduit la fréquence des cycles de nettoyage de la mémoire, ce qui peut améliorer les performances globales du serveur. Valeur entière en octets, 0 ou plus.

## AS::monitorAlertGenerator.maxOverlap - Nombre maximal de requêtes simultanées {#section-ddc6925bff944758ab19bcc9cf3f2589}

Une alerte de chevauchement est déclenchée lorsque le nombre moyen de demandes traitées simultanément pendant l’intervalle moyen dépasse ce seuil. Un chevauchement élevé peut indiquer une éventuelle situation de surcharge du serveur.

Valeur entière 1 ou supérieure. La plage type est comprise entre 20 et 50, selon le taux d’accès au cache et la complexité des requêtes.

## AS::monitorAlertGenerator.lockedThreshold - Verrouillage du seuil de requête {#section-012a1c9937d445708380339279c62d80}

Indique le nombre de secondes pendant lesquelles une requête doit être en attente avant d’être considérée comme verrouillée ou suspendue. Une alerte de requête verrouillée est émise si, à la fin d’un intervalle moyen, au moins une requête est en attente depuis plus longtemps que la période spécifiée. Valeur entière positive en ms.

Pour tenir compte des demandes de rendu et des demandes complexes qui impliquent l’obtention de données de serveurs HTTP étrangers, il est recommandé de définir cette valeur sur au moins 30 secondes (sauf si cette condition doit être détectée par cette alerte).
