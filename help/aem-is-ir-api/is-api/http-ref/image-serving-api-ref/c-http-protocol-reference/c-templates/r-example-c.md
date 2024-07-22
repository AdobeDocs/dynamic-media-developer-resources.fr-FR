---
title: Exemple C
description: Créez une application de calque "poupée de papier".
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

Créez une application de calque &quot;poupée de papier&quot;.

Une image d’arrière-plan contient la photo d’un modèle ou d’un mannequin. Les enregistrements supplémentaires dans le catalogue d’images contiennent divers accessoires et vêtements, photographiés pour correspondre au mannequin en forme et en taille.

Chaque photo d’habillement/accessoires est masquée et recadrée sur le cadre de sélection du masque afin de minimiser la taille de l’image. Les ancres et résolutions des images sont soigneusement contrôlées afin de maintenir l’alignement entre les calques et l’image d’arrière-plan. Toutes les images sont ajoutées à un catalogue d’images, avec les valeurs appropriées stockées dans les répertoires `catalog::Resolution` et `catalog::Anchor`.

Outre le calque, vous souhaitez également modifier la couleur des éléments sélectionnés. Les enregistrements de ces éléments sont prétraités afin de supprimer la couleur d’origine et d’ajuster la luminosité et le contraste d’une manière adaptée à la commande de coloration. Ce prétraitement peut être effectué hors ligne à l’aide d’un outil d’édition d’images tel qu’Adobe Photoshop ou, dans des cas simples, il peut être effectué de manière triviale en ajoutant `op_brightness=` et `op_contrast=` au champ `catalog::Modifier`.

Cette application ne justifie pas un modèle distinct, car tous les objets sont déjà correctement alignés par leurs ancres d’image ( `catalog::Anchor`) et mis à l’échelle ( `catalog::Resolution`). Il appartient au client de veiller à l’ordre approprié des calques.

Voici une requête type :

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Seule la hauteur est spécifiée. Cela permet à l’image renvoyée de varier en largeur en fonction des proportions de l’image mannequin, sans que les marges soient remplies avec la couleur d’arrière-plan.

Quelle que soit la résolution spécifiée pour chaque calque, tant qu’ils sont identiques, cela ne devrait pas avoir d’importance. Cette version peut ne pas permettre aux vues d’être plus grandes que les images composites. La définition d’une valeur de résolution élevée permet d’éviter les problèmes liés à cette limitation. L’ensemble du traitement et du compost est effectué à la résolution optimale pour la taille d’image demandée, afin d’obtenir de meilleures performances et une meilleure qualité de sortie.

Les commandes `res=` peuvent être omises si toutes les images sources ont la même résolution à grande échelle (ce qui est probablement le cas pour ce type d’application).

`rootId` doit être spécifié pour toutes les commandes `src=`, même si elles sont identiques à `rootId` spécifiées dans le chemin d’accès à l’URL.

Si aucun catalogue d’images ne doit être utilisé, il n’est pas possible d’utiliser une approche de mise à l’échelle basée sur la résolution. Dans ce cas, les facteurs d’échelle explicites doivent être calculés pour chaque élément de calque, en fonction du rapport entre les valeurs `catalog::Resolution` de chaque calque et la valeur `catalog::Resolution` de la couche d’arrière-plan. La requête de composition (avec moins de calques) peut donc se présenter comme suit :

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
