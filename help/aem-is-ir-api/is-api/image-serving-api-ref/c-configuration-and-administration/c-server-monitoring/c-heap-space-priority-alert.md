---
description: Une alerte de priorité est envoyée lorsque l’espace de tas Java gratuit est inférieur au seuil spécifié immédiatement après un cycle de collecte des déchets Java.
solution: Experience Manager
title: Alerte de priorité de l'espace de tas
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Alerte de priorité de l’espace de tas {#heap-space-priority-alert}

Une alerte de priorité est envoyée lorsque l’espace de tas Java gratuit est inférieur au seuil spécifié immédiatement après un cycle de collecte des déchets Java.

Les alertes répétées doivent être traitées en augmentant l’espace de tas Java. Les occurrences suivantes de cette condition n’entraînent pas l’envoi d’une alerte par courrier électronique tant que la période de délai spécifiée avec `AS::monitorAlertGenerator.heapSpaceResetInterval` n’est pas écoulée.
