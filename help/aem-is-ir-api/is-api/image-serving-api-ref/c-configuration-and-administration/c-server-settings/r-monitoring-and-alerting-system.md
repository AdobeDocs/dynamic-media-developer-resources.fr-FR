---
description: Utilisez ces paramètres de serveur pour configurer le système de surveillance et d'alerte.
solution: Experience Manager
title: Système de surveillance et d'alerte
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Système de surveillance et d&#39;alerte{#monitoring-and-alerting-system}

Utilisez ces paramètres de serveur pour configurer le système de surveillance et d&#39;alerte.

## AS::monitorAlertGenerator.enableGlobalAlerting - Activation du système d&#39;alertes {#section-612f8ea61794426ab205e22e5f665fa9}

Activez la notification par courrier électronique en définissant la valeur &quot;true&quot; et en configurant les paramètres de notification par courrier électronique. La définition de `false` désactive toutes les alertes par courrier électronique, ce qui peut s&#39;avérer utile lorsque vous mettez un serveur hors ligne à des fins de maintenance. Booléenne.

## AS::mailSender.host - SMTP Host {#section-151df07e7b44446581339bb7abeeba7a}

Adresse IP du serveur de messagerie SMTP.

## AS::mailSender.port- Port SMTP {#section-4b25efca8fd84d5c92dafacd0555e99d}

port d’écoute du serveur de messagerie SMTP.

## AS::monitorAlertGenerator.messageTo - Destinataire de messages {#section-0017bbaa15434117a70900c3f1163960}

Une ou plusieurs adresses électroniques auxquelles des alertes doivent être envoyées. Utilisez des points-virgules comme séparateurs.

## AS::monitorAlertGenerator.messageFrom - Expéditeur de message {#section-db320cba4ac2438ca1cfe6abce4aed87}

Adresse électronique à utiliser dans le champ **[!UICONTROL De]** courrier électronique.

## AS::monitorAlertGenerator.alertInterval - Intervalle de surveillance {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Le système de surveillance accumule les conditions d&#39;alerte pendant l&#39;intervalle d&#39;alerte et envoie un courriel d&#39;alerte contenant toutes les alertes accumulées à la fin de chaque intervalle. Millisecondes, valeur entière, 60 000 ou plus. Habituellement définie sur 5 ou 10 minutes.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Intervalle d&#39;alerte d&#39;espace de tas {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Durée minimale après une alerte d’espace de tas avant qu’une autre alerte ne soit émise. Intervalle en msec. Valeur entière, égale ou supérieure à 0.

## AS::monitorAlertGenerator.minTrafficForAlerts - Trafic minimum pour activer les alertes {#section-8b4db2d6f96642309ca35c49eb3ab230}

Demandes par seconde. Aucune alerte de temps de réponse et d’erreur ne sera émise si le trafic tombe en dessous de ce seuil. Définissez cette variable sur 0 pour envoyer des alertes de temps de réponse et d’erreur quel que soit le volume de trafic. Valeur réelle 0 ou supérieure.
