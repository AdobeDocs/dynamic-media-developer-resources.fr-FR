---
description: Quatre types généraux de vignettes de production sont pris en charge.
seo-description: Quatre types généraux de vignettes de production sont pris en charge.
seo-title: Mise à l’échelle de la vignette
solution: Experience Manager
title: Mise à l’échelle de la vignette
topic: Scene7 Image Serving - Image Rendering API
uuid: 08c8f826-7dce-4bcb-9323-4892262eb578
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Mise à l’échelle de la vignette{#vignette-scaling}

Quatre types généraux de vignettes de production sont pris en charge.

* Résolution unique

   Recommandé uniquement lorsqu’il est certain qu’une seule taille d’image de rendu est requise.
* Multi-résolution

   Recommandé lorsque toutes les tailles d’image de rendu souhaitées sont connues. Fournit une meilleure qualité et un rendu plus rapide que les vignettes à résolution unique et pyramidales, car l’image ne doit pas être mise à l’échelle après le rendu.
* Pyramide

   Il est conseillé d’opter pour plusieurs tailles d’image et de ne pas prédéfinir les tailles exactes et d’utiliser l’une des visionneuses de zoom Flash Scene7.
* Pyramide avec une ou plusieurs résolutions supplémentaires

   Offre une haute qualité pour des tailles spécifiques tout en offrant une flexibilité et la prise en charge des visionneuses de zoom.

En effet, chaque résolution est enregistrée dans la vignette de production sous la forme d’un indépendant avec sa propre largeur et hauteur d’image.

La taille  d’une vignette à résolution unique est spécifiée avec `-width` ou `-height` les deux. Si les deux valeurs sont spécifiées, la vignette est mise à l’échelle de sorte qu’aucune dimension ne soit plus grande que la taille spécifiée. Si aucune valeur n’est spécifiée, la vignette de sortie aura la même taille que la vignette d’entrée. Aucune mise à l&#39;échelle supérieure ne sera appliquée; si la taille spécifiée est supérieure à la taille de la vignette d’entrée, la vignette de sortie aura la même taille que la vignette d’entrée.

En effet, les mêmes règles s’appliquent aux vignettes à plusieurs résolutions, le premier niveau de résolution étant dimensionné comme une vignette à une seule résolution. Les résolutions supplémentaires sont spécifiées avec des valeurs séparées par des virgules supplémentaires pour `-width` ou `-height`. Il n’est pas nécessaire de trier les valeurs. Si `-width` spécifie plusieurs valeurs, `-height` vous ne devez fournir qu’une seule valeur, et inversement, dans le cas contraire, une erreur est renvoyée.

Une vignette pyramidale est créée en spécifiant `-pyramid`. Le niveau de résolution le plus élevé d’une vignette est déterminé exactement comme pour une vignette à résolution unique. Les niveaux de résolution supplémentaires sont déterminés automatiquement en redimensionnant chaque niveau à 0,5 fois le niveau précédent, le niveau le plus petit n’excédant pas 128 x 128 pixels.

Des niveaux de résolution supplémentaires peuvent être spécifiés pour une vignette pyramidale, tout comme pour une vignette multirésolution.
