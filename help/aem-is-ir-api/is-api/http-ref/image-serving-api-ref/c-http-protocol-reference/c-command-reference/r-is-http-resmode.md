---
title: Mode resMode
description: Mode Ré-échantillonnage. Choisit l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour la mise à l’échelle des données d’image. S’applique également à la rotation des calques de texte et au redimensionnement des images composites pendant la transformation de la vue.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---

# Mode resMode{#resmode}

Mode Ré-échantillonnage. Choisit l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour la mise à l’échelle des données d’image. S’applique également à la rotation des calques de texte et au redimensionnement des images composites pendant la transformation de la vue.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilen </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne l’interpolation bilinéaire standard. Méthode de rééchantillonnage la plus rapide ; Certains artefacts de crénelage sont perceptibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne l’interpolation bicubique. L’interpolation plus gourmande en ressources du processeur que l’interpolation bilinéaire, mais permet d’obtenir des images plus nettes avec des artefacts de crénelage moins visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne une fonction Fenêtre de Lanczos modifiée en tant qu’algorithme d’interpolation. Peut produire des images légèrement plus nettes que la méthode bicubique en sollicitant toutefois davantage le processeur. <span class="codeph"> sharp </span> a été remplacé par <span class="codeph"> sharp2 </span>, qui a moins de chances de provoquer des artefacts de crénelage (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bibrusque </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne Photoshop rééchantillonneur par défaut pour réduire la taille de l’image, appelé « plus net bicubique » en Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>Pour conserver les proportions d’une image lorsque vous utilisez à la fois `resMode=bisharp` et `fit=stretch`, il est recommandé d’utiliser le paramètre width ou le paramètre height. Si les deux paramètres doivent être définis, vous pouvez les placer dans un calque différent, comme illustré dans l’exemple suivant :
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Propriétés {#section-a171bacf4ddf43c782e46b86a16d443e}

Attribut de requête. S’applique à toutes les opérations de mise à l’échelle impliquées dans la création de l’image de réponse finale, y compris toute la mise à l’échelle du calque.

## Par défaut {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Exemple {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Obtenir le rendu de la meilleure qualité d’une image superposée stockée dans un catalogue d’images. L’image peut inclure du texte. L’image est ensuite traitée dans une application de retouche d’image et demande donc un canal alpha avec l’image.

` http:// *`serveur`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Voir aussi {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribut ::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
