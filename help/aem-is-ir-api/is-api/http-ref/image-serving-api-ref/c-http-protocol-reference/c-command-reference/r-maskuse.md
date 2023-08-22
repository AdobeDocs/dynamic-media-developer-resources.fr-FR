---
title: maskUse
description: Utilisation des masques d’image. Indique comment le masque ou canal alpha de l’image est utilisé pour les opérations sur l’image (par exemple, colorize=). Lorsqu’il est spécifié dans un calque d’effet, il permet d’appliquer l’effet à la zone d’arrière-plan du calque parent ou à l’ensemble du rectangle du calque parent.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# maskUse{#maskuse}

Utilisation des masques d’image. Indique comment le masque ou canal alpha de l’image est utilisé pour les opérations sur l’image (par exemple, colorize=). Lorsqu’il est spécifié dans un calque d’effet, il permet d’appliquer l’effet à la zone d’arrière-plan du calque parent ou à l’ensemble du rectangle du calque parent.

`maskUse=norm|invert|off`

Le tableau suivant illustre l’effet de `maskUse=` selon la disponibilité et le type de masque (canal alpha) associé à l&#39;image du calque.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valeur</b> </th> 
   <th class="entry"> <b> Aucun masque</b> </th> 
   <th class="entry"> <b> alpha non associé (ou image de masque distincte)</b> </th> 
   <th class="entry"> <b> alpha associé (pré-multiplié)</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> désactivé </span> </p> </td> 
   <td> <p> Rectangle d’image opaque </p> </td> 
   <td> <p> Rectangle d’image opaque </p> </td> 
   <td> <p> Zone de premier plan de l’image sur un rectangle rempli de noir uni </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> standard </span> </p> </td> 
   <td> <p> Rectangle d’image opaque </p> </td> 
   <td> <p> Zone de premier plan de l’image </p> </td> 
   <td> <p> Zone de premier plan de l’image ou du calque </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> invert </span> </p> </td> 
   <td> <p> Couche masquée </p> </td> 
   <td> <p> Zone d’arrière-plan de l’image </p> </td> 
   <td> <p> Zone d’arrière-plan de l’image ou du calque rempli de noir uni </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f36ad1af348e45aeb3eb336544df30b0}

Image ou attribut de calque. S’applique au calque 0 si `layer=comp`. Si elle est spécifiée dans un calque d’effet, la commande modifie le masque hérité du calque parent.

Le comportement de `maskUse=` n’est pas défini et n’est pas pris en charge lorsqu’il est spécifié avec du texte ou des calques de couleur unis lorsqu’aucun masque d’image n’est applicable (spécifié avec `mask=` ou `catalog::Mask`).

## Par défaut {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Exemple {#section-daa371e9be5547368ff6772342acba0a}

Colorez la zone d’arrière-plan d’une image ; le premier plan de l’image est défini par une image de masque distincte. Pour ce faire, il suffit de superposer l’arrière-plan de l’image colorée si l’image non modifiée :

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Voir aussi {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
