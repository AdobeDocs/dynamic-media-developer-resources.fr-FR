---
description: Les effets d’ombre et d’éclat des calques de style Photoshop sont mis en oeuvre à l’aide de sous-calques spéciaux (calques d’effet) qui peuvent être attachés à n’importe quel calque (le calque parent), y compris layer=0 et layer=comp.
solution: Experience Manager
title: Effets de calque
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 2%

---


# Effets de calque {#layer-effects}

Les effets d’ombre et d’éclat des calques de style Photoshop sont mis en oeuvre à l’aide de sous-calques spéciaux (calques d’effet) qui peuvent être attachés à n’importe quel calque (le calque parent), y compris layer=0 et layer=comp.

Bien que les calques d’effets prennent en charge un certain nombre d’attributs et de commandes d’image et de calque standard, ils ne sont pas destinés à être des calques à usage général et ne prennent pas en charge les données d’image ou de texte indépendantes.

Un calque parent unique peut être associé à n’importe quel nombre d’effets de calque.

## Effets intérieurs et extérieurs {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Les* effets internes sont rendus au-dessus du calque parent et ne sont visibles que dans les zones opaques du calque parent. *Les* effets externes sont rendus derrière le calque parent (de sorte qu’ils ne seront jamais visibles dans les zones opaques du calque parent) et peuvent être positionnés n’importe où dans le canevas de composition. Un effet intérieur ou extérieur est choisi en attribuant un numéro de couche d&#39;effet positif ou négatif à l&#39;aide de la commande `effect=`. La commande `effect=` contrôle également l’ordre z parmi plusieurs calques d’effets attachés au même calque parent.

## Relation avec la couche parente {#section-eb8bfc4f754a42fc973b562821d6f2d3}

Les calques d’effets sont automatiquement dimensionnés et positionnés de manière à coïncider avec le calque parent (c’est-à-dire que le calque d’effets hérite des valeurs `size=` et `origin=` du calque parent). `pos=` peut être utilisé pour éloigner le calque d’effet du calque parent, comme cela est généralement requis pour les effets de chute et d’ombre intérieure. Alors que pour les calques standard `pos=` spécifie un décalage entre les origines de ce calque et du calque 0, pour les calques d&#39;effet `pos=` spécifie le décalage entre les origines du calque d&#39;effet et du calque parent.

## Commandes et attributs pris en charge {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

Les calques d’effets acceptent les commandes et les attributs suivants :

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

## Macros d&#39;effet par défaut {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Pour faciliter l’utilisation des effets de calque, IS fournit deux macros avec le catalogue d’images par défaut, `$shadow$` et `$glow$`, qui fournissent des valeurs par défaut pour les attributs de calque d’effets semblables aux effets de calque Photoshop. Les listes de tableau suivantes qui ont un effet de commande et de macro doivent être utilisées pour implémenter les effets de calque par défaut. Naturellement, tous les attributs spécifiés dans les macros peuvent être modifiés dans l’URL ou d’autres macros peuvent être créées pour implémenter des effets de calque personnalisés.

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
   <td> <p> <span class="codeph"> effet=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Ombre intérieure </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Eclat extérieur </p> </td> 
   <td> <p> <span class="codeph"> effet=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Eclat intérieur </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples {#section-4c449fdf707b43858917fb271fa1fe96}

Ajoutez une bordure rouge de trois pixels de large avec une opacité de 50 % sur un calque :

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

La bordure suit les contours du canal alpha ou du masque de l&#39;image. La définition de `effect=1` place la bordure sur le bord intérieur à la place.

Ajoutez une ombre portée bleue sur une image à l’aide des paramètres d’effet par défaut (sauf pour la couleur) :

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` ajoute une petite marge aux bords inférieurs droits de l’image, ce qui empêche l’ombre portée d’être coupée dans les limites de l’image.

## Voir aussi {#section-1acccccf534549aea23d4c008c17e7c0}

[effet=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), Macros  [de commande%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
