---
description: Créez une application de calque "poupée de papier".
seo-description: Créez une application de calque "poupée de papier".
seo-title: Exemple C
solution: Experience Manager
title: Exemple C
topic: Scene7 Image Serving - Image Rendering API
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Exemple C{#example-c}

Créez une application de calque &quot;poupée de papier&quot;.

Une image d&#39;arrière-plan contient la photo d&#39;un mannequin ou d&#39;un mannequin. D&#39;autres enregistrements dans le catalogue d&#39;images contiennent divers vêtements et accessoires, photographiés pour correspondre au mannequin en forme et taille.

Chaque photo d’habillement ou d’accessoire est masquée et recadrée dans le cadre de sélection du masque afin de minimiser les tailles d’image. Les ancres et les résolutions d’image sont soigneusement contrôlées afin de maintenir l’alignement entre les calques et l’image d’arrière-plan. Toutes les images sont ajoutées à un catalogue d’images, avec les valeurs appropriées stockées dans `catalog::Resolution` et `catalog::Anchor`.

En plus de la superposition, nous souhaitons également modifier la couleur des éléments sélectionnés. Les enregistrements de ces éléments sont prétraités afin de supprimer la couleur d’origine et d’ajuster la luminosité et le contraste d’une manière adaptée à la commande de coloration. Ce prétraitement peut être effectué hors ligne, à l’aide d’un outil de retouche d’images tel que Photoshop, ou, dans de simples cas, il peut être effectué de manière triviale en ajoutant `op_brightness=` et `op_contrast=` au `catalog::Modifier`champ.

Cette application ne justifie pas un modèle distinct, car tous les objets sont déjà correctement alignés par leurs ancres d’image ( `catalog::Anchor`) et mis à l’échelle ( `catalog::Resolution`). Nous laissons au client le soin d’assurer l’ordre des couches approprié.

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

Seule la hauteur est spécifiée. Cela permet à l&#39;image retournée de varier en largeur selon le format de l&#39;image mannequin, sans que les marges soient remplies par la couleur d&#39;arrière-plan.

Peu importe la résolution spécifiée pour chaque calque, tant qu’ils sont tous identiques. Cette version ne permet peut-être pas aux d’être plus grands que les images composites. Spécifier une valeur de résolution élevée évite les problèmes liés à cette limitation. Tout le traitement et le montage sont effectués à la résolution optimale pour la taille d’image demandée, afin d’obtenir de meilleures performances et une meilleure qualité de sortie.

Les `res=` commandes peuvent être omises si toutes les images source ont la même résolution à pleine échelle (ce qui est probablement le cas pour ce type d’application).

Le `rootId` doit être spécifié pour toutes les `src=` commandes, même si elles sont identiques à celles `rootId` spécifiées dans le chemin d’accès de l’URL.

Si aucun catalogue d’images ne doit être utilisé, une approche de mise à l’échelle basée sur la résolution n’est pas possible. Dans ce cas, les facteurs d’échelle explicites doivent être calculés pour chaque élément de calque, en fonction du rapport entre les `catalog::Resolution` valeurs de chaque calque et la `catalog::Resolution` valeur du calque d’arrière-plan. La requête de composition (avec moins de calques) peut donc se présenter comme suit :

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

