---
description: La quantité de mémoire utilisée par le rendu d’images peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, peu de vignettes, taille et complexité des vignettes, etc.).
seo-description: La quantité de mémoire utilisée par le rendu d’images peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, peu de vignettes, taille et complexité des vignettes, etc.).
seo-title: Remarques concernant la mémoire
solution: Experience Manager
title: Remarques concernant la mémoire
topic: Scene7 Image Serving - Image Rendering API
uuid: 21247081-ff27-4237-93da-5fc996417dfd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Remarques concernant la mémoire{#memory-considerations}

La quantité de mémoire utilisée par le rendu d’images peut varier considérablement et dépend fortement de la charge et de l’utilisation réelles du serveur (par exemple, peu de vignettes, taille et complexité des vignettes, etc.).

Pour de meilleures performances, évitez d’utiliser la pagination de la mémoire (permutation).

Image Rendering partage la gestion de la mémoire d’Image Server. Lors de l’utilisation du rendu d’image, une mémoire supplémentaire doit être allouée. 30 à 50 % de la mémoire physique peuvent être raisonnables.

Pour plus d’informations sur la modification de l’allocation de mémoire du serveur d’images (ImageServer::PhysicalMemory), reportez-vous à la documentation du serveur d’images.
