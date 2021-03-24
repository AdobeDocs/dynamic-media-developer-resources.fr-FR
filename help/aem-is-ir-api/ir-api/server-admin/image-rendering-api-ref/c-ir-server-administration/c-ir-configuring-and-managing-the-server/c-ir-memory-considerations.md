---
description: La quantité de mémoire utilisée par le rendu d’images peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, peu de vignettes différentes, taille et complexité des vignettes, etc.).
solution: Experience Manager
title: Considérations relatives à la mémoire
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# Considérations relatives à la mémoire{#memory-considerations}

La quantité de mémoire utilisée par le rendu d’images peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, peu de vignettes différentes, taille et complexité des vignettes, etc.).

Pour de meilleures performances, la pagination de la mémoire (permutation) doit être évitée.

Image Rendering partage la gestion de la mémoire d’Image Server. Lors de l’utilisation du rendu d’image, une mémoire supplémentaire doit être allouée. 30 à 50 % de la mémoire physique peut être raisonnable.

Pour plus d’informations sur la modification de l’allocation de mémoire Image Server (ImageServer::PhysicalMemory), reportez-vous à la documentation relative à Image Serving.
