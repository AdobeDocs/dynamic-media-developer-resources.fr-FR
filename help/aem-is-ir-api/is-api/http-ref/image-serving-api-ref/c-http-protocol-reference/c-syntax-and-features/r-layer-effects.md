---
title: Effets de calque
description: les effets d’ombre et de lueur des calques de style Photoshop sont implémentés à l’aide de sous-calques spéciaux (calques d’effet) qui peuvent être attachés à n’importe quel calque (le calque parent), y compris calque=0 et calque=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 2%

---

# Effets de calque{#layer-effects}

les effets d’ombre et de lueur des calques de style Photoshop sont implémentés à l’aide de sous-calques spéciaux (calques d’effet) qui peuvent être attachés à n’importe quel calque (le calque parent), y compris calque=0 et calque=comp.

Bien que les calques d’effet prennent en charge un certain nombre d’attributs et de commandes de calque et d’image standard, ils ne sont pas conçus pour être des calques à usage général et ne prennent pas en charge les données d’image ou de texte indépendantes.

Vous pouvez associer un nombre illimité d&#39;effets de calque à un calque parent unique.

## Effets internes et externes {#section-2dade7ee98e041d1b4d1725e6f98a515}

*Effets internes* sont rendus sur le calque parent et ne sont visibles que dans les zones opaques du calque parent. Les *effets extérieurs* sont rendus derrière le calque parent (ils ne sont donc jamais visibles dans les zones opaques du calque parent) et peuvent être positionnés n’importe où dans la zone de travail de composition. Un effet interne ou externe est choisi en attribuant un numéro de calque d&#39;effet positif ou négatif avec la commande `effect=`. La commande `effect=` contrôle également l’ordre des z parmi plusieurs calques d’effet attachés au même calque parent.

## Relation avec le calque parent {#section-eb8bfc4f754a42fc973b562821d6f2d3}

Les calques d’effet sont automatiquement dimensionnés et positionnés de manière à coïncider avec le calque parent (en d’autres termes, le calque d’effet hérite des valeurs de `size=` et de `origin=` du calque parent). Vous pouvez utiliser `pos=` pour éloigner le calque d&#39;effet du calque parent, comme c&#39;est généralement le cas pour les effets de dépôt et d&#39;ombre interne. Alors que pour les calques standard `pos=` spécifie un décalage entre les origines de ce calque et le calque 0, pour les calques d&#39;effet `pos=` spécifie le décalage entre les origines du calque d&#39;effet et du calque parent.

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

## Macros d&#39;effet par défaut {#section-a01e8dcc87c94495b54a6dfb21d2a718}

Pour faciliter l&#39;utilisation des effets de calque, IS fournit deux macros avec le catalogue d&#39;images par défaut, `$shadow$` et `$glow$`, qui fournissent des valeurs par défaut pour les attributs de calque d&#39;effet similaires aux effets de calque Photoshop. Le tableau suivant répertorie la commande et la macro d&#39;effet à utiliser pour implémenter les effets de calque par défaut. Naturellement, vous pouvez modifier l’un des attributs spécifiés dans les macros dans l’URL ou créer d’autres macros pour implémenter des effets de calque personnalisés.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Effet souhaité </b> </th> 
   <th class="entry"> Commande <b></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Ombre portée </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Ombre intérieure </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Eclat extérieur </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Eclat intérieur </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples {#section-4c449fdf707b43858917fb271fa1fe96}

Ajoutez une bordure rouge de trois pixels de large avec une opacité de 50 % à un calque :

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

La bordure suit les contours de la couche alpha de l’image ou du masque. La définition de `effect=1` place la bordure sur le bord intérieur.

Ajoutez une ombre portée bleutée à une image à l’aide des paramètres d’effet par défaut (à l’exception de la couleur) :

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` ajoute une petite marge en bas à droite de l&#39;image, ce qui empêche l&#39;ombre portée d&#39;être écrêtée aux limites de l&#39;image.

## Voir aussi {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [Macros de commande%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
