---
description: Rotation de l’image. Fait pivoter l’image, le texte ou le calque de couleur unie selon l’angle spécifié.
seo-description: Rotation de l’image. Fait pivoter l’image, le texte ou le calque de couleur unie selon l’angle spécifié.
seo-title: rotation
solution: Experience Manager
title: rotation
topic: Scene7 Image Serving - Image Rendering API
uuid: 160d3c4b-3871-43bd-a17d-96198c7ea839
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# rotate{#rotate}

Rotation de l’image. Fait pivoter l’image, le texte ou le calque de couleur unie selon l’angle spécifié.

`rotate= *`Angle`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Angle</span> </p> </td> 
  <td class="stentry"> <p>Angle de rotation en degrés (réel). </p></td> 
 </tr> 
</table>

Les angles positifs pivotent dans le sens des aiguilles d&#39;une montre. Le point d’ancrage du calque ( `anchor=` ou `catalog::Anchor`) sert de centre de rotation. Le rectangle du calque est agrandi et ajusté autour des données pivotées, le cas échéant, pour éviter le recadrage. La rotation est appliquée après avoir rempli la zone d’arrière-plan du calque `color=`. `bgColor=` peut être utilisé pour ajouter une couleur d’arrière-plan au rectangle de délimitation après rotation.

## Propriétés {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Calque, commande. S’applique au calque actif ou au calque 0 si `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, sans rotation.

## Exemple {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Placez une étiquette &quot;A vendre&quot; près du coin supérieur gauche des images dans un catalogue d’images. La taille de l’image d’étiquette est déjà correcte pour le de 300 x 300 et doit être pivotée de 30 degrés vers la gauche. Renseignez la zone de texte avec une couleur blanche semi-opaque pour améliorer le libellé.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Nous nous appliquons `size=` à la couche 0 pour définir la taille de l’ du, plutôt que d’utiliser `wid=` et `hei=`. Cela permet `myImageId` de redimensionner sans modifier la taille finale de `labelImage`. Nous devons également spécifier `scl=1`, sinon l’image composite risque d’être redimensionnée `attribute::DefaultPix` (sauf si elle est définie sur 0,0). `color=` ajoute la couleur d’arrière-plan semi-opaque à la zone de texte avant la rotation.

Le  de des deux calques est défini sur les coins supérieur gauche pour obtenir l’alignement souhaité. Notez que le point   pour la couche 1 s’applique `labelImage`après avoir fait pivoter la couche.

Voir [l’exemple A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) pour consulter un exemple de texte avec rotation.

## Voir aussi {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
