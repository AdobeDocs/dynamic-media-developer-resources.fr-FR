---
description: Quatre types généraux de vignettes de production sont pris en charge.
solution: Experience Manager
title: Mise à l’échelle de la vignette
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---


# Mise à l’échelle de la vignette{#vignette-scaling}

Quatre types généraux de vignettes de production sont pris en charge.

* Résolution unique

   Recommandé uniquement s’il est certain qu’une seule taille d’image de rendu est requise.
* Multi-résolution

   Recommandé lorsque toutes les tailles d’image de rendu souhaitées sont connues. Fournit une meilleure qualité et un rendu plus rapide que les vignettes à résolution unique et les vignettes pyramidales, car l’image n’a pas besoin d’être mise à l’échelle après le rendu.
* Pyramide

   Il est conseillé d’utiliser toutes les fonctions, lorsque plusieurs tailles d’image sont nécessaires et que les tailles exactes ne sont pas prédéterminées et lorsque la visionneuse de zoom Dynamic Media est utilisée.
* Pyramide avec une ou plusieurs résolutions supplémentaires

   Offre une qualité élevée pour des tailles spécifiques tout en offrant une flexibilité et la prise en charge des visionneuses de zoom.

En effet, chaque résolution est enregistrée dans la vignette de production sous la forme d’une vue indépendante avec sa propre largeur et hauteur d’image.

La taille de vue d’une vignette à résolution unique est spécifiée avec `-width` ou `-height` ou les deux. Si les deux valeurs sont spécifiées, la vignette est mise à l’échelle de sorte qu’aucune dimension ne soit supérieure à la taille spécifiée. Si aucune valeur n’est spécifiée, la vignette de sortie aura la même taille que la vignette d’entrée. Aucune mise à l&#39;échelle supérieure ne sera appliquée ; si la taille spécifiée est supérieure à la taille de la vignette d’entrée, la vignette de sortie aura la même taille que la vignette d’entrée.

En effet, les mêmes règles s’appliquent aux vignettes à plusieurs résolutions, le premier niveau de résolution étant dimensionné de la même manière qu’une vignette à une seule résolution. Les résolutions supplémentaires sont spécifiées avec des valeurs séparées par des virgules supplémentaires pour `-width` ou `-height`. Il n’est pas nécessaire de trier les valeurs. Si `-width` spécifie plusieurs valeurs, `-height` ne doit fournir qu&#39;une seule valeur, et vice versa, sinon une erreur est renvoyée.

Une vignette pyramidale est créée en spécifiant `-pyramid`. Le plus grand niveau de résolution d’une vignette est déterminé exactement comme pour une vignette à résolution unique. Les niveaux de résolution supplémentaires sont déterminés automatiquement en redimensionnant chaque niveau à 0,5 fois le niveau précédent, le plus petit niveau n’excédant pas 128 x 128 pixels.

Des niveaux de résolution supplémentaires peuvent être spécifiés pour une vignette pyramidale, tout comme pour une vignette multirésolution.
