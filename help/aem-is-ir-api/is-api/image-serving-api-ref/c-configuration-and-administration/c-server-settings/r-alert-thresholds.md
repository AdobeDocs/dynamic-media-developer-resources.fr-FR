---
description: Utilisez ces paramètres de serveur pour configurer les seuils d’alerte.
solution: Experience Manager
title: Seuils d’alerte
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
TQID: 'https://experienceleague.adobe.com/mu--4-idJqrtGhbeVu3GP3LxJ4ZRL6zn1XZxTH7DLw4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 410
ht-degree: 0%

---

# Seuils d’alerte{#alert-thresholds}

Utilisez ces paramètres de serveur pour configurer les seuils d’alerte.

## AS :: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS :: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

Une alerte de temps de réponse est émise lorsque le temps moyen de traitement d&#39;une requête pendant l&#39;intervalle d&#39;échantillonnage dépasse le seuil défini ici. Exprimé en ms ; entier supérieur ou égal à 0. Les valeurs standard sont comprises entre 100 et 1 000 ms, selon la complexité des opérations.

>[!NOTE]
>
>Les requêtes qui génèrent un statut de réponse 4xx ou 5xx ne sont pas prises en compte pour cette alerte.

## AS::monitorAlertGenerator.maxErrorRate - Taux de réponse d’erreur ThresholdAS::monitorAlertGenerator.maxErrorRate - Taux de réponse d’erreur {#section-76ba77fd3102419395e0f86719a1f3ec}

Une alerte d’erreur est émise lorsque le ratio des réponses d’erreur HTTP par rapport au total des réponses pendant l’intervalle d’échantillonnage dépasse le seuil spécifié.

Valeur réelle comprise entre 0,0 et 1,0. Généralement définie sur entre 0,005 et 0,1. Définissez cette valeur sur 1 pour désactiver les alertes d’erreur.

## AS::monitorAlertGenerator.minRequestRate - Seuil de trafic faible {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Une alerte de trafic minimum est envoyée lorsque le nombre moyen de requêtes par seconde reçues pendant l’intervalle d’échantillonnage actuel tombe en dessous de ce seuil. Désactivez l’alerte en définissant cette valeur sur 0. Exprimé en requêtes par seconde. Valeur réelle égale ou supérieure à 0.

## AS::monitorAlertGenerator.minFreeHeapSpace - Seuil d’espace libre du tas {#section-ce6705045f6842769030ccb1894594cc}

Indique l’espace libre minimum du tas Java. Une alerte de priorité est envoyée immédiatement après un cycle de récupération de l’espace mémoire Java lorsque l’espace libre du tas est inférieur à ce seuil. 50 MB est recommandé pour un fonctionnement sûr du [!DNL Platform Server]. Le fait de conserver l’espace libre du tas au-dessus de cette valeur réduit la fréquence des cycles de récupération de l’espace mémoire, ce qui peut améliorer les performances globales du serveur. Valeur entière en octets, supérieure ou égale à zéro.

## AS::monitorAlertGenerator.maxOverlap - Nombre maximal de demandes simultanées {#section-ddc6925bff944758ab19bcc9cf3f2589}

Une alerte de chevauchement est déclenchée lorsque le nombre moyen de requêtes traitées simultanément au cours de l’intervalle de calcul de la moyenne dépasse ce seuil. Un chevauchement élevé peut indiquer une condition de surcharge du serveur possible.

Valeur entière 1 ou supérieure. La plage standard est comprise entre 20 et 50, selon le taux d’accès au cache et la complexité de la requête.

## AS::monitorAlertGenerator.lockedThreshold - Seuil de demande verrouillée {#section-012a1c9937d445708380339279c62d80}

Indique le nombre de secondes pendant lesquelles une demande doit être en attente avant d’être considérée comme verrouillée ou bloquée. Une alerte de requête verrouillée est émise si, à la fin d’un intervalle de calcul de moyenne, au moins une requête est en attente depuis plus longtemps que la période spécifiée. Valeur entière positive en ms.

Pour tenir compte des requêtes de rendu complexes et des requêtes impliquant l’obtention de données à partir de serveurs HTTP étrangers, il est recommandé de définir cette valeur sur au moins 30 secondes (sauf si une telle condition doit être détectée par cette alerte).
