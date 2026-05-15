---
title: maskUse
description: Utilisation du masque d’image. Indique comment le masque ou la couche alpha de l’image est utilisé pour les opérations sur l’image (par exemple, colorize=). Lorsqu’il est spécifié dans un calque d’effet, il permet d’appliquer l’effet à la zone d’arrière-plan du calque parent ou au rectangle entier du calque parent.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
TQID: 'https://experienceleague.adobe.com/swX7HTiWiAhQlPu9f7Qsay2htiJcxnxOCMeu7YlrCm8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 1%

---

# maskUse{#maskuse}

Utilisation du masque d’image. Indique comment le masque ou la couche alpha de l’image est utilisé pour les opérations sur l’image (par exemple, colorize=). Lorsqu’il est spécifié dans un calque d’effet, il permet d’appliquer l’effet à la zone d’arrière-plan du calque parent ou au rectangle entier du calque parent.

`maskUse=norm|invert|off`

Le tableau suivant illustre l’effet de la `maskUse=` en fonction de la disponibilité et du type du masque (couche alpha) associé à l’image de calque.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valeur </b> </th> 
   <th class="entry"> <b> Aucun masque</b> </th> 
   <th class="entry"> <b> Alpha non associé (ou image de masque distincte)</b> </th> 
   <th class="entry"> <b> alpha associé (pré-multiplié)</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> de </span> </p> </td> 
   <td> <p> Rectangle d’image opaque </p> </td> 
   <td> <p> Rectangle d’image opaque </p> </td> 
   <td> <p> Zone de premier plan de l’image sur un rectangle plein de noir </p> </td> 
  </tr> 
  <tr> 
   <td> <p> </span> de norme <span class="codeph"> </p> </td> 
   <td> <p> Rectangle d’image opaque </p> </td> 
   <td> <p> Zone de premier plan de l’image </p> </td> 
   <td> <p> Zone de premier plan de l’image ou du calque </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> inverser le </span> </p> </td> 
   <td> <p> Calque masqué </p> </td> 
   <td> <p> Zone d’arrière-plan de l’image </p> </td> 
   <td> <p> Zone d’arrière-plan de l’image ou du calque rempli de noir uni </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f36ad1af348e45aeb3eb336544df30b0}

Attribut d’image ou de calque. S’applique au calque 0 si `layer=comp`. Si un calque d’effet le spécifie, la commande modifie le masque hérité du calque parent.

Le comportement de `maskUse=` n’est pas défini et n’est pas pris en charge lorsqu’il est spécifié avec du texte ou des calques de couleur unie lorsqu’aucun masque d’image n’est applicable (spécifié avec `mask=` ou `catalog::Mask`).

## Par défaut {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Exemple {#section-daa371e9be5547368ff6772342acba0a}

Colorisez la zone d’arrière-plan d’une image ; le premier plan de l’image est défini par une image de masque distincte. Pour ce faire, superposez l’arrière-plan de l’image colorée sur l’image non modifiée :

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Voir aussi {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
