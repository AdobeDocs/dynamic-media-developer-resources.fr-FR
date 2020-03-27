---
description: Pour manipuler un graphique, vous pouvez utiliser les points de référence qui rappellent les points cardinaux.
seo-description: Pour manipuler un graphique, vous pouvez utiliser les points de référence qui rappellent les points cardinaux.
seo-title: Protocole serveur FXG
solution: Experience Manager
title: Protocole serveur FXG
topic: Scene7 Image Serving - Image Rendering API
uuid: 5cb123ca-2274-4ddb-8fa1-ab22a19172f6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# Protocole serveur FXG{#fxg-server-protocol}

Pour manipuler un graphique, vous pouvez utiliser les points de référence qui rappellent les points cardinaux.

Avec les points de référence, vous pouvez faire pivoter, mettre à l’échelle ou redimensionner un graphique par rapport à un point de référence particulier. Les points de référence sont `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`,  et . `south``southeast` Par exemple, avec le point de référence centre, vous pouvez faire pivoter un graphique de 45 degrés sur son centre. This illustration shows where the reference points are located, a graphic, the graphic rotated 20 degrees from its `northWest` reference point, and the graphic rotated 20 degrees from its `east` reference point.

![](assets/wp_ref_points.png)

* A. Emplacements des points de référence
* B. Un graphique
* C. The graphic rotated 20 degrees from its `northWest` reference point
* D. The graphic rotated 20 degrees from its `east` reference point

La syntaxe est la suivante :

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

La valeur par défaut est none. The `inherit` value passes the `s7:referencePoint` value, provided it is not `none`, from the top of the page or group level to all children. The `none` setting means that there is no reference point for the object and the FXG coordinate system is used.

>[!NOTE]
>
>pour utiliser un point de référence et éviter tout déplacement de l’objet après sa manipulation, mettez à jour les valeurs x et y après l’avoir manipulé.

Lorsqu’une valeur de `s7:referencePoint` est utilisée avec les groupes (ou chemins, éléments de trait ou tout élément sans définition de hauteur et de largeur explicite), la valeur s’applique au cadre de sélection cumulatif du groupe. For example, the top-left point of the bounding box of all the objects in the group serves as the `northWest` reference point for the group; the bottom-right point serves as the `southEast` reference point.

