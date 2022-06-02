---
title: resMode
description: Mode Rééchantillonnage. Choisit l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour le dimensionnement des données d’image. S’applique également à la rotation des calques de texte et au redimensionnement des images composites lors de la transformation de la vue.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 3%

---

# resMode{#resmode}

Mode Rééchantillonnage. Choisit l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour le dimensionnement des données d’image. S’applique également à la rotation des calques de texte et au redimensionnement des images composites lors de la transformation de la vue.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Sélection de l’interpolation binaire standard. méthode de rééchantillonnage la plus rapide; certains artefacts de crénelage sont visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne l’interpolation bicubique. Plus intensif en processeur que l’interpolation bi-linéaire, mais produit des images plus nettes avec des artefacts de crénelage plus discrets. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne une fonction Lanczos Window modifiée comme algorithme d’interpolation. Peut produire des résultats légèrement plus nets que le bi-cube à un coût CPU plus élevé. <span class="codeph"> sharp </span> a été remplacé par <span class="codeph"> sharp2 </span>, qui a une probabilité moindre de provoquer des artefacts de crénelage (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Sélectionnez le rééchantillonneur Photoshop par défaut pour réduire la taille de l’image, appelé "Bicubique plus net" dans Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>Pour conserver les proportions d’une image lorsque vous utilisez les deux `resMode=bisharp` et `fit=stretch`, il est recommandé d’utiliser le paramètre de largeur ou de hauteur. Si les deux paramètres doivent être définis, vous pouvez les encapsuler dans un autre calque, comme illustré dans l’exemple suivant :
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Propriétés {#section-a171bacf4ddf43c782e46b86a16d443e}

Attribut de requête. S’applique à toutes les opérations de mise à l’échelle impliquées dans la création de l’image de réponse finale, y compris la mise à l’échelle de tous les calques.

## Par défaut {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Exemple {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Récupérez un rendu de meilleure qualité d’une image superposée stockée dans un catalogue d’images. L’image peut contenir du texte. L’image est ensuite traitée dans une application d’édition d’image et demande donc un canal alpha avec l’image.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Voir aussi {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
