---
description: Une alerte de priorité est envoyée lorsque l’espace libre du tas Java est inférieur au seuil spécifié immédiatement après un cycle de récupération de l’espace mémoire Java.
solution: Experience Manager
title: Alerte de priorité de l’espace de tas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
TQID: 'https://experienceleague.adobe.com/zCx9aodQa-gcTc0iFuK3N0fJf43EdyCWk8cYIawYPaM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 0%

---

# Alerte de priorité de l’espace de tas{#heap-space-priority-alert}

Une alerte de priorité est envoyée lorsque l’espace libre du tas Java est inférieur au seuil spécifié immédiatement après un cycle de récupération de l’espace mémoire Java.

Les alertes répétées doivent être traitées en augmentant l’espace du tas Java. Les occurrences suivantes de cette condition ne génèrent pas d’alerte par e-mail tant que le délai spécifié avec `AS::monitorAlertGenerator.heapSpaceResetInterval` n’a pas expiré.
