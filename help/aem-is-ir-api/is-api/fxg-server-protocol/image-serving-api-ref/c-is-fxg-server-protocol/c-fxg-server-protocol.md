---
title: Protocole du serveur FXG
description: Pour manipuler un graphique, vous pouvez utiliser les points de référence qui rappellent les points cardinaux.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
TQID: 'https://experienceleague.adobe.com/DXmhIshiUYoP-BlVe5cJFXbII9sEIdyo5YDkoKP-t0w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 28%

---

# Protocole du serveur FXG{#fxg-server-protocol}

Pour manipuler un graphique, vous pouvez utiliser les points de référence qui rappellent les points cardinaux.

Avec les points de référence, vous pouvez faire pivoter, mettre à l’échelle ou redimensionner un graphique par rapport à un point de référence particulier. Les points de référence sont `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` et `southeast`. Par exemple, en utilisant le point de référence central, vous pouvez faire pivoter un graphique de 45° par rapport à son centre. L&#39;image suivante montre l&#39;emplacement des points de référence, un graphique, le graphique pivoté de 20° par rapport à son point de référence `northWest` et le graphique pivoté de 20° par rapport à son point de référence `east`.

![Image des points de référence](assets/wp_ref_points.png)

* A. Emplacements des points de référence
* B. Un graphique
* C. Le graphique a pivoté de 20° par rapport à son point de référence `northWest`
* D. Le graphique a pivoté de 20° par rapport à son point de référence `east`

La syntaxe est la suivante :

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

La valeur par défaut est aucune. La valeur `inherit` transmet la valeur `s7:referencePoint`, à condition qu’elle ne soit pas `none`, du haut de la page ou au niveau du groupe à tous les enfants. Le paramètre `none` signifie qu&#39;il n&#39;y a pas de point de référence pour l&#39;objet et que le repère FXG est utilisé.

>[!NOTE]
>
>pour utiliser un point de référence et éviter tout déplacement de l’objet après sa manipulation, mettez à jour les valeurs x et y après l’avoir manipulé.

Lorsqu’une valeur de `s7:referencePoint` est utilisée avec des groupes (ou des chemins, des éléments de ligne ou tout élément qui n’a pas de définitions explicites de largeur et de hauteur), la valeur s’applique au rectangle de délimitation cumulé du groupe. Par exemple, le point supérieur gauche du cadre de sélection de tous les objets du groupe sert de point de référence `northWest` pour le groupe ; le point inférieur droit sert de point de référence `southEast`.
