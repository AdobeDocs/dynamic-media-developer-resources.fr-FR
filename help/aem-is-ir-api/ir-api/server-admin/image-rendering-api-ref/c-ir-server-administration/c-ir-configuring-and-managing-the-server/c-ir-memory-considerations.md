---
description: La quantité de mémoire utilisée par le rendu d’image peut varier considérablement et dépend largement de la charge et de l’utilisation réelles du serveur (par exemple, peu de vignettes, taille et complexité des vignettes, etc.).
solution: Experience Manager
title: Remarques relatives à la mémoire
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Remarques relatives à la mémoire{#memory-considerations}

La quantité de mémoire utilisée par le rendu d’image peut varier considérablement et dépend largement de la charge et de l’utilisation réelles du serveur (par exemple, peu de vignettes, taille et complexité des vignettes, etc.).

Pour de meilleures performances, la pagination de la mémoire (permutation) doit être évitée.

Image Rendering partage la gestion de la mémoire du serveur d’images. Lors de l’utilisation du rendu d’image, une mémoire supplémentaire doit être allouée. 30 à 50 % de la mémoire physique peuvent être raisonnables.

Reportez-vous à la documentation du serveur d’images pour plus d’informations sur la modification de l’allocation de mémoire du serveur d’images (ImageServer::PhysiqueMemory).
