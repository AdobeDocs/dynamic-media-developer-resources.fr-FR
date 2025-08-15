---
description: Quatre types généraux de vignettes de production sont pris en charge.
solution: Experience Manager
title: Dimensionnement de la vignette
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f9f92254-41d8-4d22-a168-78b49dd55478
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Dimensionnement de la vignette{#vignette-scaling}

Quatre types généraux de vignettes de production sont pris en charge.

* Résolution unique

  Recommandé uniquement lorsqu’il est certain qu’une seule taille d’image de rendu est requise.
* Multi-résolution

  Recommandé lorsque toutes les tailles d’image de rendu souhaitées sont connues. Fournit un rendu de meilleure qualité et plus rapide que les vignettes pyramidales et à résolution unique, car l’image n’a pas besoin d’être mise à l’échelle après rendu.
* Pyramide

  Idéal à toutes fins, recommandé lorsque plusieurs tailles d’image sont nécessaires et que les tailles exactes ne sont pas prédéterminées, ainsi que lorsque la visionneuse Zoom Dynamic Media est utilisée.
* Pyramide avec une ou plusieurs résolutions supplémentaires

  Fournit une qualité élevée pour des tailles spécifiques tout en offrant flexibilité et prise en charge de la visionneuse avec zoom.

En effet, chaque résolution est enregistrée dans la vignette de production en tant que vue indépendante avec sa propre largeur et sa propre hauteur d’image.

La taille d’affichage d’une vignette à résolution unique est spécifiée avec `-width`, `-height` ou les deux. Si les deux valeurs sont spécifiées, la vignette est mise à l’échelle de sorte qu’aucune dimension ne soit plus grande que la taille spécifiée. Si aucune valeur n’est spécifiée, la vignette de sortie a la même taille que la vignette d’entrée. Aucune mise à l’échelle n’est appliquée. Si la taille spécifiée est supérieure à la taille de la vignette d’entrée, la vignette de sortie a la même taille que la vignette d’entrée.

En fait, les mêmes règles s’appliquent aux vignettes à résolution multiple, le premier niveau de résolution étant dimensionné comme une vignette à résolution unique. Les résolutions supplémentaires sont spécifiées avec des valeurs supplémentaires séparées par des virgules pour `-width` ou `-height`. Les valeurs n’ont pas besoin d’être triées. Si `-width` spécifie plusieurs valeurs, `-height` ne devez fournir qu’une seule valeur, et vice versa, sinon une erreur est renvoyée.

Une vignette pyramidale est créée en spécifiant `-pyramid`. Le niveau de résolution le plus élevé d&#39;une telle vignette est déterminé exactement comme pour une vignette à simple résolution. Les niveaux de résolution supplémentaires sont déterminés automatiquement en mettant à l’échelle chaque niveau de 0,5 fois le niveau précédent, le plus petit niveau ne dépassant pas 128 x 128 pixels.

Des niveaux de résolution supplémentaires peuvent être spécifiés pour une vignette pyramidale, comme pour une vignette multi-résolution.
