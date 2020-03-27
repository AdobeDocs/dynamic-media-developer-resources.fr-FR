---
description: Utilisez ces paramètres de serveur pour configurer les seuils d’alerte.
seo-description: Utilisez ces paramètres de serveur pour configurer les seuils d’alerte.
seo-title: Seuils d’alerte
solution: Experience Manager
title: Seuils d’alerte
topic: Scene7 Image Serving - Image Rendering API
uuid: 032cb396-1a03-4ba9-82d6-ed2cb06e8cf2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Seuils d’alerte{#alert-thresholds}

Utilisez ces paramètres de serveur pour configurer les seuils d’alerte.

## AS : monitorAlertGenerator.maxAverageResponseTime -Seuil du temps de réponse AS : monitorAlertGenerator.maxAverageResponseTime -Temps de réponse {#section-35111039ac6c4a63ba23fc2c828ab726}

Une alerte de temps de réponse est émise lorsque la durée moyenne de traitement d’une requête pendant l’intervalle d’échantillonnage dépasse le seuil défini ici. Exprimé en msec; entier 0 ou supérieur. Les valeurs types sont comprises entre 100 et 1 000 msec, selon la complexité des opérations.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Les requêtes qui génèrent un état de réponse 4xx ou 5xx ne sont pas prises en compte pour cette alerte.

## AS::monitorAlertGenerator.maxErrorRate - Seuil de réponse aux erreursAS::monitorAlertGenerator.maxErrorRate - Taux de réponse aux erreurs {#section-76ba77fd3102419395e0f86719a1f3ec}

Une alerte d’erreur est émise lorsque le rapport entre les réponses d’erreur HTTP et le nombre total de réponses au cours de l’intervalle d’échantillonnage dépasse le seuil spécifié.

Valeur réelle comprise entre 0.0 et 1.0.Généralement définie entre 0.005 et 0.1. Définissez cette variable sur 1 pour désactiver les alertes d’erreur.

## AS::monitorAlertGenerator.minRequestRate - Seuil de trafic faible {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Une alerte de trafic minimale est envoyée lorsque le nombre moyen de demandes reçues par seconde au cours de l’intervalle d’échantillonnage actuel est inférieur à ce seuil. Désactivez l&#39;alerte en définissant cette valeur sur 0. Exprimé dans les requêtes par seconde. Valeur réelle 0 ou supérieure.

## AS::monitorAlertGenerator.minFreeHeapSpace -Seuil d’espace de tas libre {#section-ce6705045f6842769030ccb1894594cc}

Spécifie l’espace de tas Java gratuit minimum. Une alerte de priorité est envoyée immédiatement après un cycle de collecte des déchets Java lorsque l’espace libre du tas est inférieur à ce seuil. 50 Mo est recommandé pour un fonctionnement sécurisé du serveur de plateformes. Si vous maintenez l’espace libre du tas au-dessus de cette valeur, vous réduisez la fréquence des cycles de collecte des déchets, ce qui peut améliorer les performances globales du serveur. Valeur entière en octets, 0 ou plus.

## AS::monitorAlertGenerator.maxOverlap - Nombre maximal de requêtes simultanées {#section-ddc6925bff944758ab19bcc9cf3f2589}

Une alerte de chevauchement est déclenchée lorsque le nombre moyen de requêtes traitées simultanément au cours de l’intervalle moyen dépasse ce seuil. Un chevauchement élevé peut indiquer une surcharge potentielle du serveur.

Valeur entière 1 ou supérieure. La plage type est comprise entre 20 et 50, selon le taux d’accès au cache et la complexité des requêtes.

## AS::monitorAlertGenerator.lockThreshold - Seuil de requête verrouillé {#section-012a1c9937d445708380339279c62d80}

Indique le nombre de secondes pendant lesquelles une requête doit être en attente avant d’être considérée comme verrouillée ou bloquée. Une alerte de requête verrouillée est émise si, à la fin d’un intervalle moyen, au moins une requête est en attente depuis plus longtemps que la période spécifiée. Valeur entière positive en msec.

Pour tenir compte des requêtes et requêtes de rendu complexes qui impliquent l’obtention de données à partir de serveurs HTTP étrangers, il est recommandé de définir cette valeur sur au moins 30 secondes (sauf si cette condition doit être détectée par cette alerte).
