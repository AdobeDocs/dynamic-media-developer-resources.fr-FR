---
description: Une alerte de priorité est envoyée lorsque l’espace de tas Java gratuit est inférieur au seuil spécifié immédiatement après un cycle de collecte des déchets Java.
seo-description: Une alerte de priorité est envoyée lorsque l’espace de tas Java gratuit est inférieur au seuil spécifié immédiatement après un cycle de collecte des déchets Java.
seo-title: Alerte de priorité de l'espace de tas
solution: Experience Manager
title: Alerte de priorité de l'espace de tas
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Alerte de priorité de l’espace de tas {#heap-space-priority-alert}

Une alerte de priorité est envoyée lorsque l’espace de tas Java gratuit est inférieur au seuil spécifié immédiatement après un cycle de collecte des déchets Java.

Les alertes répétées doivent être traitées en augmentant l’espace de tas Java. Les occurrences suivantes de cette condition n’entraînent pas l’envoi d’une alerte par courrier électronique tant que la période de délai spécifiée avec `AS::monitorAlertGenerator.heapSpaceResetInterval` n’est pas écoulée.
