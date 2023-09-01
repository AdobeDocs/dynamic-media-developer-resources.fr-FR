---
title: perspective
description: Transformation de la perspective. Appliquez une transformation de perspective à l’image source du calque afin qu’elle remplisse la région spécifiée avec le quadrilatéral. D’autres zones du calque restent transparentes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---

# perspective{#perspective}

Transformation de la perspective. Appliquez une transformation de perspective à l’image source du calque afin qu’elle remplisse la région spécifiée avec le quadrilatéral. D’autres zones du calque restent transparentes.

`perspective= *`mener à bien`*[, *`resOptions`*]`

`perspectiveN= *`axisQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> mener à bien</span> </p></td> 
  <td class="stentry"> <p>Coordonnées quadrilatérales en perspective (8 réelles, séparées par des virgules). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> axisQuadN</span> </p></td> 
  <td class="stentry"> <p>Coordonnées quadrilatérales normalisées de la perspective (8 réelles, séparées par des virgules). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Options de rééchantillonnage (voir ci-dessous). </p></td> 
 </tr> 
</table>

Le modificateur *`perspQuad`* se compose de quatre valeurs de coordonnées de pixel dans l’espace de coordonnées composite (ou de couche 0), qui provient du coin supérieur gauche de l’image composite.

Le modificateur `perspQuadN` se compose de quatre valeurs de coordonnées normalisées, où `0.0,0.0` correspond au coin supérieur gauche de l’image composite/de couche 0 et `1.0,1.0` dans le coin inférieur droit.

L’image d’entrée est transformée de sorte que le coin supérieur gauche de l’image d’entrée correspond à la première valeur de coordonnée de `perspQuad[N]`, le coin supérieur droit de la seconde coordonnée, le coin inférieur droit de la troisième coordonnée et le coin inférieur gauche de la quatrième coordonnée.

>[!NOTE]
>
>Le modificateur `pos=` peut être utilisé pour positionner davantage le calque transformé dans l’image composite.

Les coordonnées quadrilatérales de la perspective peuvent se trouver en dehors de l’image composite.

Le comportement n’est pas défini si le quadrilatère ne convient pas à une transformation de perspective. Par exemple, si deux ou plusieurs sommets correspondent, si trois ou tous les sommets se trouvent sur la même ligne, ou si le quadrilatère est auto-intersection ou concave.

## Considérations sur la qualité {#section-7cc9056afa614300a9b8844d39739fc3}

Bien que l’implémentation par défaut produise un compromis raisonnable entre la qualité et les performances, il peut être nécessaire d’augmenter la résolution de l’image source pour améliorer la netteté ou de la réduire pour réduire les artefacts de crénelage.

Si la source est une image, utilisez `scale=` pour choisir une résolution différente (par rapport à la résolution complète de l’image). La valeur spécifiée `scale=` est arrondie au niveau de résolution PTIF supérieur suivant. S’il existe une source de requête imbriquée, la taille de l’image générée par la requête imbriquée peut être ajustée pour obtenir la netteté souhaitée. Pour les calques de texte, la résolution de l’image d’entrée (le texte rendu) est ajustée en sélectionnant une valeur size= plus grande avec une résolution accrue spécifiée avec `textAttr=`.

Le modificateur *`resOptions`* vous permet de sélectionner un autre algorithme de rééchantillonnage. Les valeurs suivantes sont prises en charge (respect de la casse) :

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
   <td> <p> Suréchantillonnage standard (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> Suréchantillonnage avec instabilité variable (<span class="varname"> n</span> doit être une valeur entière comprise entre 0 et 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-818e57df0a1b4449888543bc6af77751}

Couche, commande. S’applique au calque actif ou au calque 0 si `layer=comp`. Ignoré par les calques d’effet.

Le modificateur `res=` est toujours ignoré lorsque la perspective est présente dans le même calque. Le modificateur `size=` est ignoré lorsqu’il est spécifié pour les calques d’image. Les modificateurs `size=` et `res=` dans les calques avec `perspective=` sont réservés à une utilisation ultérieure.

## Par défaut {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, sans transformation de perspective.

## Voir aussi {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
