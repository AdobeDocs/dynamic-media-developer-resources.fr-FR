---
description: Utilisez ces paramètres du serveur pour configurer le système de surveillance et d’alerte.
solution: Experience Manager
title: Système de surveillance et d'alerte
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Système de surveillance et d&#39;alerte{#monitoring-and-alerting-system}

Utilisez ces paramètres du serveur pour configurer le système de surveillance et d’alerte.

## AS::monitorAlertGenerator.enableGlobalAlerting - Activation du système d’alerte {#section-612f8ea61794426ab205e22e5f665fa9}

Activez les notifications par e-mail en définissant sur « true » et en configurant les paramètres de notification par e-mail. La définition sur `false` désactive toutes les alertes par e-mail. Cela peut s’avérer utile lors de la mise hors ligne d’un serveur à des fins de maintenance. Booléen.

## AS::mailSender.host - Hôte SMTP {#section-151df07e7b44446581339bb7abeeba7a}

Adresse IP du serveur de messagerie SMTP.

## AS::mailSender.port- Port SMTP {#section-4b25efca8fd84d5c92dafacd0555e99d}

Port d’écoute du serveur de messagerie SMTP.

## AS::monitorAlertGenerator.messageTo - Destinataire du message {#section-0017bbaa15434117a70900c3f1163960}

Une ou plusieurs adresses e-mail auxquelles les alertes doivent être envoyées. Utilisez des points-virgules comme séparateurs.

## AS::monitorAlertGenerator.messageFrom - Expéditeur du message {#section-db320cba4ac2438ca1cfe6abce4aed87}

Adresse électronique à utiliser dans le champ d’adresse électronique **[!UICONTROL De]**.

## AS::monitorAlertGenerator.alertInterval - Intervalle de surveillance {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Le système de surveillance accumule les conditions d&#39;alerte pendant l&#39;intervalle d&#39;alerte et envoie un e-mail d&#39;alerte contenant toutes les alertes accumulées à la fin de chaque intervalle. Millisecondes, valeur entière, 60000 ou supérieure. Réglez généralement sur 5 ou 10 minutes.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Intervalle d’alerte de l’espace de tas {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Durée minimale après l’émission d’une alerte d’espace de tas avant qu’une autre alerte ne soit émise. Durée de l’intervalle en ms. Valeur entière, supérieure ou égale à 0.

## AS::monitorAlertGenerator.minTrafficForAlerts - Trafic minimum pour activer les alertes {#section-8b4db2d6f96642309ca35c49eb3ab230}

Demandes par seconde. Aucun temps de réponse et aucune alerte d’erreur ne sont émis si le trafic tombe sous ce seuil. Définissez cette valeur sur 0 pour envoyer le temps de réponse et les alertes d’erreur, quel que soit le volume de trafic. Valeur réelle égale ou supérieure à 0.
