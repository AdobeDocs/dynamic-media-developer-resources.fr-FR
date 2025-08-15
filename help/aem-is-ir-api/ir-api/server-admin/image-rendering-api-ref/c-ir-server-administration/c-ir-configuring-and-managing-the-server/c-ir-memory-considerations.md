---
description: La quantité de mémoire utilisée par le rendu d’image peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, quelques vignettes par rapport à de nombreuses vignettes différentes, taille et complexité des vignettes, etc.).
solution: Experience Manager
title: Considérations relatives à la mémoire
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Considérations relatives à la mémoire{#memory-considerations}

La quantité de mémoire utilisée par le rendu d’image peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, quelques vignettes par rapport à de nombreuses vignettes différentes, taille et complexité des vignettes, etc.).

Pour de meilleures performances, la pagination de la mémoire (permutation) doit être évitée.

Le rendu d’image partage la gestion de la mémoire du serveur d’images. Lors de l’utilisation du rendu d’image, de la mémoire supplémentaire doit être allouée. 30 à 50% de la mémoire physique peut être raisonnable.

Reportez-vous à la documentation du service d’images pour plus d’informations sur la modification de l’allocation de mémoire du serveur d’images (ImageServer::PhysicalMemory).
