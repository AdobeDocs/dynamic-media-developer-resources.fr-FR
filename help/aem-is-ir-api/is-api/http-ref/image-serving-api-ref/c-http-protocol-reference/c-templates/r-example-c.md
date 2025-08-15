---
title: Exemple C
description: Créez une application de superposition « poupée de papier ».
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Exemple C{#example-c}

Créez une application de superposition « poupée de papier ».

Une image d’arrière-plan contient la photo d’un modèle ou d’un mannequin. Les enregistrements supplémentaires du catalogue d&#39;images contiennent divers vêtements et accessoires, photographiés pour correspondre au mannequin en forme et en taille.

Chaque photo de vêtement/accessoire est masquée et recadrée dans le cadre de sélection du masque afin de réduire la taille des images. Les ancres d’image et les résolutions sont soigneusement contrôlées afin de maintenir l’alignement entre les calques et l’image d’arrière-plan. Toutes les images sont ajoutées à un catalogue d’images, avec les valeurs appropriées stockées dans `catalog::Resolution` et `catalog::Anchor`.

Outre le calque, vous pouvez également modifier la couleur des éléments sélectionnés. Les enregistrements de ces éléments sont prétraités pour supprimer la couleur d&#39;origine et ajuster la luminosité et le contraste d&#39;une manière appropriée à la commande de coloration. Ce prétraitement peut être effectué hors ligne, à l’aide d’un outil d’édition d’images tel qu’Adobe Photoshop, ou, dans les cas les plus simples, de manière triviale en ajoutant `op_brightness=` et `op_contrast=` au champ `catalog::Modifier`.

Cette application ne garantit pas un modèle distinct, car tous les objets sont déjà correctement alignés par leurs ancres d’image ( `catalog::Anchor`) et mis à l’échelle ( `catalog::Resolution`). C’est au client ou à la cliente de s’assurer que l’ordre des couches est approprié.

Une requête type peut se présenter comme suit :

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Seule la hauteur est spécifiée. Cela permet à l’image renvoyée de varier en largeur en fonction des proportions de l’image du mannequin, sans obtenir de marges remplies avec la couleur d’arrière-plan.

La résolution spécifiée pour chaque calque n’a pas d’importance, à condition qu’elles soient toutes identiques. Cette version peut ne pas permettre que les vues soient plus grandes que les images composites. La spécification d’une valeur de résolution élevée évite les problèmes liés à cette limitation. Tout le traitement et la composition sont effectués à la résolution optimale pour la taille d’image demandée, afin d’obtenir de meilleures performances et une qualité de sortie optimale.

Les commandes `res=` peuvent être omises si toutes les images sources ont la même résolution à grande échelle (ce qui est probablement le cas pour ce type d’application).

La `rootId` doit être spécifiée pour toutes les commandes `src=`, même si elles sont identiques à la `rootId` spécifiée dans le chemin d’accès à l’URL.

Si aucun catalogue d’images ne doit être utilisé, une approche de mise à l’échelle basée sur la résolution n’est pas possible. Dans ce cas, des facteurs d’échelle explicites doivent être calculés pour chaque élément de calque, en fonction du rapport entre les valeurs `catalog::Resolution` pour chaque calque et la valeur `catalog::Resolution` du calque d’arrière-plan. La requête de composition (avec moins de calques) peut donc se présenter comme suit :

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
