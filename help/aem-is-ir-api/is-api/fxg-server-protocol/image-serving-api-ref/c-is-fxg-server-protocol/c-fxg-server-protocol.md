---
title: Protocole du serveur FXG
description: Pour manipuler un graphique, vous pouvez utiliser des points de référence similaires à des points de boussole.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 18%

---

# Protocole du serveur FXG{#fxg-server-protocol}

Pour manipuler un graphique, vous pouvez utiliser des points de référence similaires à des points de boussole.

Avec les points de référence, vous pouvez faire pivoter, mettre à l’échelle ou redimensionner un graphique par rapport à un point de référence particulier. Les points de référence sont `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` et `southeast`. Par exemple, en utilisant le point de référence central, vous pouvez faire pivoter un graphique de 45° sur son centre. L’image suivante montre l’emplacement des points de référence, un graphique, l’image a pivoté de 20° à partir de son point de référence `northWest` et l’image a pivoté de 20° à partir de son point de référence `east`.

![Image de points de référence](assets/wp_ref_points.png)

* A. Emplacements des points de référence
* B. Un graphique
* C. Le graphique a pivoté de 20° depuis son point de référence `northWest`
* D. Le graphique a pivoté de 20° depuis son point de référence `east`

La syntaxe est la suivante :

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

La valeur par défaut est none. La valeur `inherit` transmet la valeur `s7:referencePoint`, à condition qu’elle ne soit pas `none`, du haut de la page ou au niveau du groupe à tous les enfants. Le paramètre `none` signifie qu’il n’existe aucun point de référence pour l’objet et que le système de coordonnées FXG est utilisé.

>[!NOTE]
>
>pour utiliser un point de référence et éviter tout déplacement de l’objet après sa manipulation, mettez à jour les valeurs x et y après l’avoir manipulé.

Lorsqu’une valeur de `s7:referencePoint` est utilisée avec des groupes (ou chemins, éléments de ligne ou tout élément qui n’a pas de définitions de largeur et de hauteur explicites), la valeur s’applique au cadre de sélection cumulatif du groupe. Par exemple, le point supérieur gauche du cadre de sélection de tous les objets du groupe sert de point de référence `northWest` pour le groupe ; le point inférieur droit sert de point de référence `southEast`.
