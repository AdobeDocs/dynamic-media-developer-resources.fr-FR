---
title: perspective
description: Transformation en perspective. Appliquez une transformation en perspective à l'image source du calque afin qu'elle remplisse la région spécifiée avec le quadrilatère. D'autres zones de la couche restent transparentes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
TQID: 'https://experienceleague.adobe.com/XfQCa-7NeORdGGLEc247lv-HQb99vuDE-31hmMuUUGM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 477
ht-degree: 0%

---

# perspective{#perspective}

Transformation en perspective. Appliquez une transformation en perspective à l&#39;image source du calque afin qu&#39;elle remplisse la région spécifiée avec le quadrilatère. D&#39;autres zones de la couche restent transparentes.

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Coordonnées en pixels du quadrilatère en perspective (8 références, séparées par des virgules). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Coordonnées normalisées en perspective quadrilatérale (8 réels, séparés par des virgules). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Options de rééchantillonnage (voir ci-dessous). </p></td> 
 </tr> 
</table>

Le modificateur *`perspQuad`* se compose de quatre valeurs de coordonnées en pixels dans l’espace de coordonnées composite (ou calque 0), qui provient du coin supérieur gauche de l’image composite.

Le modificateur `perspQuadN` se compose de quatre valeurs de coordonnées normalisées, où `0.0,0.0` correspond au coin supérieur gauche de l’image composite/calque 0 et `1.0,1.0` au coin inférieur droit.

L&#39;image d&#39;entrée est transformée de sorte que le coin supérieur gauche de l&#39;image d&#39;entrée soit mappé à la première valeur de coordonnée de `perspQuad[N]`, le coin supérieur droit à la deuxième coordonnée, le coin inférieur droit à la troisième coordonnée et le coin inférieur gauche à la quatrième coordonnée.

>[!NOTE]
>
>Le modificateur `pos=` peut être utilisé pour positionner davantage le calque transformé dans l’image composite.

Les coordonnées quadrilatérales en perspective peuvent être situées à l&#39;extérieur de l&#39;image composite.

Le comportement n&#39;est pas défini si le quadrilatère ne convient pas à une transformation en perspective. Par exemple, si deux sommets ou plus coïncident, si trois sommets ou tous les sommets sont sur la même ligne, ou si le quadrilatère se croise ou est concave.

## Considérations de qualité {#section-7cc9056afa614300a9b8844d39739fc3}

Bien que l’implémentation par défaut produise un compromis raisonnable entre la qualité et les performances, il peut être nécessaire d’augmenter la résolution de l’image source pour améliorer la netteté ou de la réduire pour réduire les artefacts de alias.

Si la source est une image, utilisez `scale=` pour choisir une résolution différente (par rapport à la résolution complète de l’image). La valeur `scale=` spécifiée est arrondie au niveau de résolution PTIF supérieur suivant. S’il existe une source de requête imbriquée, la taille de l’image produite par la requête imbriquée peut être ajustée pour obtenir la netteté souhaitée. Pour les calques de texte, la résolution de l’image d’entrée (le texte rendu) est ajustée en sélectionnant une valeur size= plus grande avec une résolution plus élevée spécifiée par `textAttr=`.

Le modificateur *`resOptions`* permet de sélectionner un autre algorithme de rééchantillonnage. Les valeurs suivantes sont prises en charge (respect de la casse) :

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valeur </b> </th> 
   <th class="entry"> <b> Description </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> Le plus proche voisin. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> Bilinéaire. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> Super-échantillonnage standard (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> Super-échantillonnage avec gigue réglable (<span class="varname"> n</span> doit être une valeur entière comprise entre 0 et 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-818e57df0a1b4449888543bc6af77751}

Commande Calque. S’applique au calque actif ou au calque 0, le cas `layer=comp`. Ignoré par les calques d’effet.

Le modificateur `res=` est toujours ignoré lorsque la perspective est présente dans le même calque. Le modificateur `size=` est ignoré lorsqu’il est spécifié pour les calques d’image. Les modificateurs `size=` et `res=` dans les calques avec `perspective=` sont réservés pour une utilisation ultérieure.

## Par défaut {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, pas de transformation en perspective.

## Voir aussi {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
