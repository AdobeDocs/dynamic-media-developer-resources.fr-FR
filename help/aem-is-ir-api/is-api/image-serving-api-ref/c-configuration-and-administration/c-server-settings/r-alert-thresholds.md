---
description: Utilisez ces paramètres de serveur pour configurer des seuils d'alerte.
solution: Experience Manager
title: Seuils d’alerte
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---


# Seuils d&#39;alerte {#alert-thresholds}

Utilisez ces paramètres de serveur pour configurer des seuils d&#39;alerte.

## AS : monitorAlertGenerator.maxAverageResponseTime -Seuil de temps de réponse AS: monitorAlertGenerator.maxAverageResponseTime -Temps de réponse {#section-35111039ac6c4a63ba23fc2c828ab726}

Une alerte de temps de réponse est émise lorsque la durée moyenne de traitement d’une requête au cours de l’intervalle d’échantillonnage dépasse le seuil défini ici. Exprimé en msec ; entier 0 ou supérieur. Les valeurs types sont comprises entre 100 et 1 000 msec, selon la complexité des opérations.

>[!NOTE]
>
>Les requêtes qui génèrent un état de réponse 4xx ou 5xx ne sont pas prises en compte pour cette alerte.

## AS::monitorAlertGenerator.maxErrorRate - Error Response Rate Threshold::monitorAlertGenerator.maxErrorRate - Error Response Rate {#section-76ba77fd3102419395e0f86719a1f3ec}

Une alerte d’erreur est émise lorsque le rapport entre les réponses d’erreur HTTP et le nombre total de réponses au cours de l’intervalle d’échantillonnage dépasse le seuil spécifié.

Valeur réelle comprise entre 0.0 et 1.0.Généralement définie entre 0.005 et 0.1. Définissez cette valeur sur 1 pour désactiver les alertes d&#39;erreur.

## AS::monitorAlertGenerator.minRequestRate - Faible seuil de trafic {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Une alerte de trafic minimale est envoyée lorsque le nombre moyen de demandes reçues par seconde au cours de l’intervalle d’échantillonnage actuel est inférieur à ce seuil. Désactivez l&#39;alerte en définissant cette valeur sur 0. Exprimé en requêtes par seconde. Valeur réelle 0 ou supérieure.

## AS::monitorAlertGenerator.minFreeHeapSpace -Free Heap Space Seuil d&#39;espace de tas libre {#section-ce6705045f6842769030ccb1894594cc}

Indique l’espace de tas Java gratuit minimum. Une alerte de priorité est envoyée immédiatement après un cycle de collecte des déchets Java lorsque l’espace de tas libre est inférieur à ce seuil. 50 Mo est recommandé pour un fonctionnement sûr de Platform Server. Le fait de maintenir l’espace libre de tas au-dessus de cette valeur réduit la fréquence des cycles de collecte des déchets, ce qui peut améliorer les performances globales du serveur. Valeur entière en octets, 0 ou plus.

## AS::monitorAlertGenerator.maxOverlap - Nombre maximal de requêtes simultanées {#section-ddc6925bff944758ab19bcc9cf3f2589}

Une alerte de chevauchement est déclenchée lorsque le nombre moyen de requêtes traitées simultanément au cours de l’intervalle de moyenne dépasse ce seuil. Un chevauchement élevé peut indiquer une éventuelle surcharge du serveur.

Valeur entière 1 ou supérieure. La plage type est comprise entre 20 et 50, en fonction du taux d’accès au cache et de la complexité des requêtes.

## AS::monitorAlertGenerator.lockThreshold - Seuil de demande verrouillé {#section-012a1c9937d445708380339279c62d80}

Indique le nombre de secondes pendant lesquelles une requête doit être en attente avant d’être considérée comme verrouillée ou suspendue. Une alerte de demande verrouillée est émise si, à la fin d’un intervalle moyen, au moins une demande est en attente depuis plus longtemps que la période spécifiée. Valeur entière positive en msec.

Pour tenir compte des requêtes et requêtes de rendu complexes qui impliquent l’obtention de données à partir de serveurs HTTP étrangers, il est recommandé de définir cette valeur sur au moins 30 secondes (à moins qu’une telle condition ne soit détectée par cette alerte).
