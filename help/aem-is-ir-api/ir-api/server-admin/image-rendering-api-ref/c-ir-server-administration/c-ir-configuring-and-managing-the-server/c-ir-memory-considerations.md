---
description: La quantité de mémoire utilisée par le rendu d’images peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, peu de vignettes différentes, taille et complexité des vignettes, etc.).
seo-description: La quantité de mémoire utilisée par le rendu d’images peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, peu de vignettes différentes, taille et complexité des vignettes, etc.).
seo-title: Considérations relatives à la mémoire
solution: Experience Manager
title: Considérations relatives à la mémoire
topic: Scene7 Image Serving - Image Rendering API
uuid: 21247081-ff27-4237-93da-5fc996417dfd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# Considérations relatives à la mémoire{#memory-considerations}

La quantité de mémoire utilisée par le rendu d’images peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, peu de vignettes différentes, taille et complexité des vignettes, etc.).

Pour de meilleures performances, la pagination de la mémoire (permutation) doit être évitée.

Image Rendering partage la gestion de la mémoire d’Image Server. Lors de l’utilisation du rendu d’image, une mémoire supplémentaire doit être allouée. 30 à 50 % de la mémoire physique peut être raisonnable.

Pour plus d’informations sur la modification de l’allocation de mémoire Image Server (ImageServer::PhysicalMemory), reportez-vous à la documentation relative à Image Serving.
