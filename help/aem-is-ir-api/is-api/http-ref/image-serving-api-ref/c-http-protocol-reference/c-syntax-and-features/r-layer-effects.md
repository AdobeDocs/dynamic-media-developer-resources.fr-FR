---
description: Les effets d’ombre et d’éclat de calque de style Photoshop sont implémentés à l’aide de sous-calques spéciaux (calques d’effet) qui peuvent être joints à n’importe quel calque (calque parent), y compris layer=0 et layer=comp.
solution: Experience Manager
title: Effets de calque
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 2%

---

# Effets de calque{#layer-effects}

Les effets d’ombre et d’éclat de calque de style Photoshop sont implémentés à l’aide de sous-calques spéciaux (calques d’effet) qui peuvent être joints à n’importe quel calque (calque parent), y compris layer=0 et layer=comp.

Bien que les calques d’effet prennent en charge un certain nombre d’attributs et de commandes d’image et de calque standard, ils ne sont pas destinés à des calques d’usage général et ne prennent pas en charge les données d’image ou de texte indépendantes.

Un seul calque parent peut contenir un nombre indéfini d’effets de calque.

## Effets internes et externes {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Les* effets internes sont rendus au-dessus du calque parent et ne sont visibles que dans les zones opaques du calque parent. *Les* effets externes sont rendus derrière le calque parent (ils ne seront donc jamais visibles dans les zones opaques du calque parent) et peuvent être positionnés n’importe où dans la zone de travail du compositeur. Un effet intérieur ou extérieur est choisi en attribuant un numéro de couche d’effet positif ou négatif avec la commande `effect=`. La commande `effect=` contrôle également l’ordre z parmi plusieurs calques d’effet attachés à la même couche parent.

## Relation avec le calque parent {#section-eb8bfc4f754a42fc973b562821d6f2d3}

Les calques d’effet sont automatiquement dimensionnés et positionnés pour coïncider avec le calque parent (c’est-à-dire que le calque d’effet hérite des valeurs `size=` et `origin=` du calque parent). `pos=` peut être utilisé pour éloigner le calque d’effet du calque parent, comme cela est généralement nécessaire pour les effets de chute et d’ombre intérieure. Tandis que pour les calques standard `pos=` spécifie un décalage entre les origines de ce calque et le calque 0, pour les calques d’effet `pos=` spécifie le décalage entre les origines du calque d’effet et le calque parent.

## Commandes et attributs pris en charge {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

Les calques d’effet acceptent les commandes et attributs suivants :

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

Toutes les autres commandes d’image et de calque contenues dans les calques d’effet sont ignorées.

## Macros d’effet par défaut {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Pour faciliter l’utilisation des effets de calque, IS fournit deux macros avec le catalogue d’images par défaut, `$shadow$` et `$glow$`, qui fournissent des valeurs par défaut pour les attributs de calque d’effet similaires aux effets de calque Photoshop. Le tableau suivant répertorie la commande d’effet et la macro à utiliser pour implémenter les effets de calque par défaut. Naturellement, l’un des attributs spécifiés dans les macros peut être modifié dans l’URL ou d’autres macros peuvent être créées pour implémenter des effets de calque personnalisés.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Effet souhaité</b> </th> 
   <th class="entry"> <b> Commande</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Ombre portée </p> </td> 
   <td> <p> <span class="codeph"> Effet=-1&amp;$ombre$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Ombre intérieure </p> </td> 
   <td> <p> <span class="codeph"> Effet=1&amp;$ombre$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Eclat extérieur </p> </td> 
   <td> <p> <span class="codeph"> effet=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Eclat intérieur </p> </td> 
   <td> <p> <span class="codeph"> Effet=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples {#section-4c449fdf707b43858917fb271fa1fe96}

Ajoutez une bordure rouge de trois pixels de large avec une opacité de 50 % à un calque :

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

La bordure suit les contours du canal alpha ou masque de l&#39;image. Si vous définissez `effect=1`, la bordure est placée sur le bord intérieur.

Ajoutez une ombre portée bleue à une image à l’aide des paramètres d’effet par défaut (sauf pour la couleur) :

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` ajoute une petite marge aux bords inférieurs droit de l’image, ce qui empêche l’ombre portée d’être tronquée aux limites de l’image.

## Voir aussi {#section-1acccccf534549aea23d4c008c17e7c0}

[effet=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), Macros  [de commande%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
