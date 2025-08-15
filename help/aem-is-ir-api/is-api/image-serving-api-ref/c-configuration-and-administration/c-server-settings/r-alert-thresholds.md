---
description: Utilisez ces paramètres de serveur pour configurer les seuils d’alerte.
solution: Experience Manager
title: Seuils d’alerte
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Seuils d’alerte{#alert-thresholds}

Utilisez ces paramètres de serveur pour configurer les seuils d’alerte.

## AS :: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS :: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

Une alerte de temps de réponse est émise lorsque le délai moyen de traitement d’une demande pendant l’intervalle d’échantillonnage dépasse le seuil défini ici. Exprimé en msc ; Entier 0 ou plus. Les valeurs typiques sont comprises entre 100 et 1000 msec, selon la complexité des opérations.

>[!NOTE]
>
>Les demandes qui entraînent un état de réponse 4xx ou 5xx ne sont pas prises en compte pour cette alerte.

## AS ::monitorAlertGenerator.maxErrorRate - Seuil du taux de réponse aux erreursAS ::monitorAlertGenerator.maxErrorRate - Taux de réponse aux erreurs {#section-76ba77fd3102419395e0f86719a1f3ec}

Une alerte d’erreur est émise lorsque le rapport entre les réponses d’erreur HTTP et le nombre total de réponses pendant l’intervalle d’échantillonnage dépasse le seuil spécifié.

Valeur réelle comprise entre 0,0 et 1,0.Généralement définie sur 0,005 à 0,1. Définissez ce paramètre sur 1 pour désactiver les alertes d’erreur.

## AS ::monitorAlertGenerator.minRequestRate - Seuil de trafic inférieur {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Une alerte de trafic minimal est envoyée lorsque le nombre moyen de demandes par seconde reçues pendant l’intervalle d’échantillonnage actuel tombe en dessous de ce seuil. Désactivez l’alerte en définissant cette valeur sur 0. Exprimé en demandes par seconde. Valeur réelle égale ou supérieure à zéro.

## AS ::monitorAlertGenerator.minFreeHeapSpace -Seuil d’espace de tas libre {#section-ce6705045f6842769030ccb1894594cc}

Spécifie l’espace minimum libre du tas Java. Une alerte de priorité est envoyée immédiatement après un cycle de nettoyage de la mémoire Java lorsque l’espace de tas libre est inférieur à ce seuil. 50 Mo sont recommandés pour un fonctionnement sûr du [!DNL Platform Server]. Maintenir l’espace de tas libre au-dessus de cette valeur réduit la fréquence des cycles de nettoyage de la mémoire, ce qui peut améliorer les performances globales du serveur. Valeur entière en octets, 0 ou plus.

## AS ::monitorAlertGenerator.maxOverlap - Nombre maximal de demandes simultanées {#section-ddc6925bff944758ab19bcc9cf3f2589}

Une alerte de chevauchement est déclenchée lorsque le nombre moyen de demandes traitées simultanément pendant l’intervalle de calcul de la moyenne dépasse ce seuil. Un chevauchement élevé peut indiquer une condition de surcharge possible du serveur.

Valeur entière supérieure ou égale à 1. La plage habituelle est de 20 à 50, selon le taux d’accès au cache et la compatibilité des demandes.

## AS ::monitorAlertGenerator.lockedThreshold - Seuil de demandes verrouillées {#section-012a1c9937d445708380339279c62d80}

Spécifie le nombre de secondes qu’une demande doit être en attente avant d’être considérée comme verrouillée ou bloquée. Une alerte de demande verrouillée est émise si, à la fin d’un intervalle de calcul de la moyenne, au moins une demande est en attente depuis plus longtemps que la période spécifiée. Valeur entière positive en mssec.

Pour tenir compte des demandes de rendu complexes et des requêtes qui impliquent l’obtention de données à partir de serveurs HTTP étrangers, il est recommandé de définir cette valeur sur au moins 30 secondes (sauf si une telle condition doit être détectée par cette alerte).
