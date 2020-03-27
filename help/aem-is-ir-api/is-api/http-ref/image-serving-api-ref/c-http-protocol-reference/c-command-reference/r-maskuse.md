---
description: Utilisation des masques d’image. Indique comment le masque ou le alpha de l’image est utilisé pour les opérations sur l’image (par exemple, colorize=). Lorsqu’il est spécifié dans un calque d’effet, il permet d’appliquer l’effet à la zone d’arrière-plan du calque parent ou à l’ensemble du rectangle du calque parent.
seo-description: Utilisation des masques d’image. Indique comment le masque ou le alpha de l’image est utilisé pour les opérations sur l’image (par exemple, colorize=). Lorsqu’il est spécifié dans un calque d’effet, il permet d’appliquer l’effet à la zone d’arrière-plan du calque parent ou à l’ensemble du rectangle du calque parent.
seo-title: maskUse
solution: Experience Manager
title: maskUse
topic: Scene7 Image Serving - Image Rendering API
uuid: 2c70da87-f869-495a-be50-226a4516e002
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# maskUse{#maskuse}

Utilisation des masques d’image. Indique comment le masque ou le alpha de l’image est utilisé pour les opérations sur l’image (par exemple, colorize=). Lorsqu’il est spécifié dans un calque d’effet, il permet d’appliquer l’effet à la zone d’arrière-plan du calque parent ou à l’ensemble du rectangle du calque parent.

`maskUse=norm|invert|off`

Le tableau suivant illustre l’effet de `maskUse=` selon la disponibilité et le type du masque (alpha) associé à l’image du calque.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valeur</b> </th> 
   <th class="entry"> <b> Aucun masque</b> </th> 
   <th class="entry"> <b> Alpha non associé (ou image de masque distincte)</b> </th> 
   <th class="entry"> <b> Alpha associé (prémultiplié)</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> désactivé </span> </p> </td> 
   <td> <p> Rectangle d’image opaque </p> </td> 
   <td> <p> Rectangle d’image opaque </p> </td> 
   <td> <p> Zone de premier plan de l’image sur un rectangle rempli de noir plein </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norme </span> </p> </td> 
   <td> <p> Rectangle d’image opaque </p> </td> 
   <td> <p> Zone de premier plan de l’image </p> </td> 
   <td> <p> Zone de premier plan de l’image ou du calque </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> inverser </span> </p> </td> 
   <td> <p> Calque masqué </p> </td> 
   <td> <p> Zone d’arrière-plan de l’image </p> </td> 
   <td> <p> Zone d’arrière-plan de l’image ou du calque rempli de noir uni </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f36ad1af348e45aeb3eb336544df30b0}

Attribut d’image ou de calque. S’applique au calque 0 si `layer=comp`. Si elle est spécifiée dans un calque d’effet, la commande modifie le masque hérité du calque parent.

Le comportement de `maskUse=` est non défini et non pris en charge lorsqu’il est spécifié avec du texte ou des calques de couleur unie lorsqu’aucun masque d’image n’est applicable (spécifié avec `mask=` ou `catalog::Mask`).

## Par défaut {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Exemple {#section-daa371e9be5547368ff6772342acba0a}

Coloriser la zone d’arrière-plan d’une image ; le premier plan de l’image est défini par une image de masque distincte. Pour ce faire, superposez l’arrière-plan de l’image colorée au-dessus de l’image non modifiée :

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Voir aussi {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
