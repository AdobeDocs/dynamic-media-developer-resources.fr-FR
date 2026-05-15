---
description: La quantité de mémoire utilisée par le rendu d’image peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, quelques vignettes par rapport à de nombreuses vignettes différentes, taille et complexité des vignettes, etc.).
solution: Experience Manager
title: Considérations relatives à la mémoire
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
TQID: 'https://experienceleague.adobe.com/l41dx4mMn82TvImVVCJJKgJZbP-mWT5KbnzfZ5xFJqg'
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
source-wordcount: 129
ht-degree: 0%

---

# Considérations relatives à la mémoire{#memory-considerations}

La quantité de mémoire utilisée par le rendu d’image peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, quelques vignettes par rapport à de nombreuses vignettes différentes, taille et complexité des vignettes, etc.).

Pour de meilleures performances, la pagination de la mémoire (permutation) doit être évitée.

Le rendu d’image partage la gestion de la mémoire du serveur d’images. Lors de l’utilisation du rendu d’image, de la mémoire supplémentaire doit être allouée. 30 à 50% de la mémoire physique peut être raisonnable.

Reportez-vous à la documentation du service d’images pour plus d’informations sur la modification de l’allocation de mémoire du serveur d’images (ImageServer::PhysicalMemory).
