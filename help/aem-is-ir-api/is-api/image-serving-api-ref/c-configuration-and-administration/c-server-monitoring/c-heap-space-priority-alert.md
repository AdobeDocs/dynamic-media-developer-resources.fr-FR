---
description: Une alerte de priorité est envoyée lorsque l’espace libre du tas Java est inférieur au seuil spécifié immédiatement après un cycle de nettoyage de la mémoire Java.
solution: Experience Manager
title: Alerte de priorité de l’espace du tas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# Alerte de priorité de l’espace du tas{#heap-space-priority-alert}

Une alerte de priorité est envoyée lorsque l’espace libre du tas Java est inférieur au seuil spécifié immédiatement après un cycle de nettoyage de la mémoire Java.

Les alertes répétées doivent être résolues en augmentant l’espace du tas Java. Les occurrences ultérieures de cette condition n’entraînent pas une alerte par e-mail tant que la période de délai spécifiée avec `AS::monitorAlertGenerator.heapSpaceResetInterval` n’a pas expiré.
