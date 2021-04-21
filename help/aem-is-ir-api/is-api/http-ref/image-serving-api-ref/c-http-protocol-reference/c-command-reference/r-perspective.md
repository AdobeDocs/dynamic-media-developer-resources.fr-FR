---
description: Transformation de la perspective. Appliquez une transformation de perspective à l’image source du calque pour remplir la région spécifiée par le quadrilatère. D’autres zones du calque restent transparentes.
solution: Experience Manager
title: perspective
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 2%

---


# perspective{#perspective}

Transformation de la perspective. Appliquez une transformation de perspective à l’image source du calque pour remplir la région spécifiée par le quadrilatère. D’autres zones du calque restent transparentes.

`perspective= *``*[, *`OptionsQuadresReportSuite`*]`

`perspectiveN= *`Options `*[, *`de recherchede donnéesQuadNres`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ΔQuad</span> </p></td> 
  <td class="stentry"> <p>Coordonnées quadrilatérales en perspective (8 réelles, séparées par des virgules). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ΔQuadN</span> </p></td> 
  <td class="stentry"> <p>Coordonnées quadrilatérales en perspective normalisées (8 réelles, séparées par des virgules). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Options de rééchantillonnage (voir ci-dessous). </p></td> 
 </tr> 
</table>

*`perspQuad`* se compose de quatre valeurs de coordonnées de pixels dans l’espace de coordonnées composite (ou calque 0), qui provient du coin supérieur gauche de l’image composite.

`perspQuadN` se compose de quatre valeurs de coordonnées normalisées, où  `0.0,0.0` correspond au coin supérieur gauche de l’image composite/calque 0 et  `1.0,1.0` au coin inférieur droit.

L’image d’entrée est transformée de sorte que le coin supérieur gauche de l’image d’entrée correspond à la première valeur de coordonnée `perspQuad[N]`, à l’angle supérieur droit de la seconde coordonnée, à l’angle inférieur droit de la troisième coordonnée et à l’angle inférieur gauche de la quatrième coordonnée.

>[!NOTE]
>
>`pos=` peut être utilisé pour positionner davantage le calque transformé dans l’image composite.

Les coordonnées quadrilatérales de la perspective peuvent être situées à l&#39;extérieur de l&#39;image composite.

Le comportement n&#39;est pas défini si le quadrilatère ne convient pas à une transformation de perspective (par exemple, si deux sommets ou plus coïncident, si trois sommets ou tous se trouvent sur la même ligne, ou si le quadrilatère est auto-intersection ou concave).

## Considérations relatives à la qualité {#section-7cc9056afa614300a9b8844d39739fc3}

Bien que l’implémentation par défaut produise un compromis raisonnable entre la qualité et les performances, il peut parfois être nécessaire d’augmenter la résolution de l’image source pour améliorer la netteté ou de la réduire pour réduire les artefacts de crénelage.

Si la source est une image, utilisez `scale=` pour choisir une résolution différente (par rapport à la résolution complète de l’image). La valeur `scale=` spécifiée est arrondie au niveau de résolution PTIF supérieur suivant. Dans le cas d’une source de requête imbriquée, la taille de l’image produite par la requête imbriquée peut être ajustée pour obtenir la netteté souhaitée. Pour les calques de texte, la résolution de l’image d’entrée (le texte rendu) est ajustée en sélectionnant une valeur size= plus grande tout en augmentant la résolution spécifiée par `textAttr=`.

*`resOptions`* permet de sélectionner un autre algorithme de rééchantillonnage. Les valeurs suivantes sont prises en charge (sensible à la casse) :

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valeur</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> Le voisin le plus proche. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> Bilinéaire. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> Superéchantillonnage standard (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3<span class="varname"> Tn</span></span> </p> </td> 
   <td> <p> Le super-échantillonnage avec instabilité réglable (<span class="varname"> n</span> doit être une valeur entière comprise entre 0 et 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-818e57df0a1b4449888543bc6af77751}

Calque, commande. S&#39;applique au calque actif ou au calque 0 si `layer=comp`. Ignoré par les calques d’effet.

`res=` est toujours ignorée lorsque la perspective est présente dans le même calque. `size=` est ignorée lorsqu’elle est spécifiée pour les calques d’image. `size=` et  `res=` dans les calques avec  `perspective=` sont réservés pour une utilisation ultérieure.

## Par défaut {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, sans transformation de perspective.

## Voir aussi {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ,  [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065),  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
