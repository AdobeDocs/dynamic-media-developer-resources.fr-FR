---
description: Pour manipuler un graphique, vous pouvez utiliser les points de référence qui rappellent les points cardinaux.
solution: Experience Manager
title: Protocole du serveur FXG
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 48%

---

# Protocole du serveur FXG{#fxg-server-protocol}

Pour manipuler un graphique, vous pouvez utiliser les points de référence qui rappellent les points cardinaux.

Avec les points de référence, vous pouvez faire pivoter, mettre à l’échelle ou redimensionner un graphique par rapport à un point de référence particulier. Les points de référence sont `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` et `southeast`. Par exemple, avec le point de référence centre, vous pouvez faire pivoter un graphique de 45 degrés sur son centre. Cette illustration indique l’emplacement des points de référence, un graphique, le graphique a pivoté de 20 degrés par rapport à son point de référence `northWest` et le graphique a pivoté de 20 degrés par rapport à son point de référence `east`.

![](assets/wp_ref_points.png)

* A. Emplacements des points de référence
* B. Un graphique
* C. Le graphique a pivoté de 20 degrés par rapport à son point de référence `northWest`
* D. Le graphique a pivoté de 20 degrés par rapport à son point de référence `east`

La syntaxe est la suivante :

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

La valeur par défaut est none. La valeur `inherit` transmet la valeur `s7:referencePoint`, à condition qu’elle ne soit pas `none`, depuis le haut de la page ou au niveau du groupe, à tous les enfants. Le paramètre `none` signifie qu’il n’existe aucun point de référence pour l’objet et que le système de coordonnées FXG est utilisé.

>[!NOTE]
>
>pour utiliser un point de référence et éviter tout déplacement de l’objet après sa manipulation, mettez à jour les valeurs x et y après l’avoir manipulé.

Lorsqu’une valeur de `s7:referencePoint` est utilisée avec les groupes (ou chemins, éléments de trait ou tout élément sans définition de hauteur et de largeur explicite), la valeur s’applique au cadre de sélection cumulatif du groupe. Par exemple, le point supérieur gauche du cadre de sélection de tous les objets du groupe sert de point de référence `northWest` au groupe. le point inférieur droit sert de point de référence `southEast`.
