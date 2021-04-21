---
description: Créez une application de calage "poupée de papier".
solution: Experience Manager
title: Exemple C
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Exemple C{#example-c}

Créez une application de calage &quot;poupée de papier&quot;.

Une image d&#39;arrière-plan contient la photo d&#39;un mannequin ou d&#39;un mannequin. D&#39;autres enregistrements dans le catalogue d&#39;images contiennent divers vêtements et accessoires, photographiés pour correspondre au mannequin en forme et taille.

Chaque photo d’habillement/accessoire est masquée et recadrée dans le cadre de sélection du masque afin de minimiser les tailles d’image. Les ancres et les résolutions d’image sont soigneusement contrôlées afin de maintenir l’alignement entre les calques et l’image d’arrière-plan, et toutes les images sont ajoutées à un catalogue d’images, avec les valeurs appropriées stockées dans `catalog::Resolution` et `catalog::Anchor`.

En plus de la superposition, nous voulons aussi modifier la couleur des éléments sélectionnés. Les enregistrements de ces éléments sont prétraités afin de supprimer la couleur d’origine et d’ajuster la luminosité et le contraste d’une manière adaptée à la commande de coloration. Ce prétraitement peut être effectué hors ligne, à l’aide d’un outil d’édition d’images tel que Photoshop ou, dans de simples cas, il peut être effectué de manière triviale en ajoutant `op_brightness=` et `op_contrast=` au champ `catalog::Modifier`.

Cette application ne justifie pas un modèle distinct, car tous les objets sont déjà correctement alignés par leurs ancres d’image ( `catalog::Anchor`) et mis à l’échelle ( `catalog::Resolution`). Nous laissons au client le soin d&#39;assurer l&#39;ordre approprié des couches.

Voici à quoi peut ressembler une requête type :

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Seule la hauteur est spécifiée. Cela permet à l&#39;image retournée de varier en largeur selon le format de l&#39;image mannequin, sans que les marges soient remplies avec la couleur d&#39;arrière-plan.

Peu importe la résolution spécifiée pour chaque calque, à condition qu’elles soient toutes identiques. Cette version peut ne pas permettre aux vues d’être plus grandes que les images composites. Spécifier une valeur de résolution élevée évite les problèmes liés à cette limitation. Le traitement et le montage se font à la résolution optimale pour la taille d’image demandée, afin d’obtenir de meilleures performances et une meilleure qualité de sortie.

Les commandes `res=` peuvent être omises si toutes les images source ont la même résolution à pleine échelle (ce qui est probablement le cas pour ce type d&#39;application).

`rootId` doit être spécifié pour toutes les commandes `src=`, même si elles sont identiques à `rootId` spécifiées dans le chemin d&#39;accès de l&#39;URL.

Si aucun catalogue d’images ne doit être utilisé, une approche de mise à l’échelle basée sur la résolution n’est pas possible. Dans ce cas, les facteurs d&#39;échelle explicites doivent être calculés pour chaque élément de calque, en fonction du rapport entre les valeurs `catalog::Resolution` de chaque calque et la valeur `catalog::Resolution` de la couche d&#39;arrière-plan. La demande de composition (avec moins de calques) peut donc ressembler à ceci :

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

