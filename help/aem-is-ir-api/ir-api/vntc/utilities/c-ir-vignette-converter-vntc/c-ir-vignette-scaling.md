---
description: Quatre types généraux de vignettes de production sont pris en charge.
solution: Experience Manager
title: Mise à l’échelle des vignettes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f9f92254-41d8-4d22-a168-78b49dd55478
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Mise à l’échelle des vignettes{#vignette-scaling}

Quatre types généraux de vignettes de production sont pris en charge.

* Résolution unique

   Recommandé uniquement lorsqu’il est certain qu’une seule taille d’image de rendu est requise.
* Multi-résolution

   Recommandé lorsque toutes les tailles d’image de rendu souhaitées sont connues. Offre une meilleure qualité et un rendu plus rapide que les vignettes à résolution unique et pyramidale, car l’image n’a pas besoin d’être mise à l’échelle après le rendu.
* Pyramide

   L’objectif est idéal lorsque plusieurs tailles d’image sont nécessaires et que les tailles exactes ne sont pas prédéterminées et lorsque la visionneuse de zoom Dynamic Media est utilisée.
* Pyramide avec une ou plusieurs résolutions supplémentaires

   Offre une qualité élevée pour des tailles spécifiques tout en offrant une flexibilité et la prise en charge de la visionneuse de zoom.

En fait, chaque résolution est enregistrée dans la vignette de production sous la forme d’une vue indépendante avec sa propre largeur et hauteur d’image.

La taille d’affichage d’une vignette à une seule résolution est spécifiée à l’aide de l’option `-width` ou `-height` ou les deux. Si les deux valeurs sont indiquées, la vignette est mise à l’échelle de sorte qu’aucune dimension ne soit plus grande que la taille spécifiée. Si aucune valeur n’est spécifiée, la vignette de sortie aura la même taille que la vignette d’entrée. Aucune mise à l’échelle supérieure n’est appliquée ; si la taille spécifiée est supérieure à la taille de la vignette d’entrée, la vignette de sortie aura la même taille que la vignette d’entrée.

En fait, les mêmes règles s’appliquent aux vignettes à plusieurs résolutions, le premier niveau de résolution étant dimensionné comme une vignette à une seule résolution. Les résolutions supplémentaires sont spécifiées avec des valeurs séparées par des virgules supplémentaires pour l’une ou l’autre des `-width` ou `-height`. Il n’est pas nécessaire de trier les valeurs. If `-width` spécifie plusieurs valeurs, puis `-height` ne doit fournir qu’une seule valeur, et vice versa, sinon une erreur est renvoyée.

Une vignette pyramidale est créée en spécifiant `-pyramid`. Le niveau de résolution le plus élevé d’une vignette est déterminé exactement comme pour une vignette à résolution unique. Les niveaux de résolution supplémentaires sont déterminés automatiquement en mettant à l’échelle chaque niveau à 0,5 fois le niveau précédent, avec un niveau le plus petit ne dépassant pas 128x128 pixels.

Des niveaux de résolution supplémentaires peuvent être spécifiés pour une vignette pyramidale, comme pour une vignette à plusieurs résolutions.
