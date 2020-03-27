---
description: Calque  .
seo-description: Calque  .
seo-title: ' '
solution: Experience Manager
title: ' '
topic: Scene7 Image Serving - Image Rendering API
uuid: a36fc0b6-7744-4c1c-b9f8-4aa31a886bff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# origin{#origin}

Calque  .

`origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>Décalage des pixels à partir du coin supérieur gauche du rect de calque (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Décalage normalisé à partir du centre du rect de calque (réel, réel). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>Le calque rect inclut toujours toute modification par `extend=`.

Définit le point d’alignement du rectangle du calque, qui est utilisé pour positionner le rectangle du calque par rapport au calque 0 par `pos=`. `originN=0,0` positionne le calque   au centre du rectangle du calque. `originN=-0.5,-0.5` et `origin=0,0` est l’angle supérieur gauche, `originN=0.5,0.5` l’angle inférieur droit du rectangle du calque.

## Propriétés {#section-60f639e36ada43d1abc6bfc100afc925}

Attribut de calque. S’applique au calque actif ou au calque 0 si `layer=comp`. Non affecté par les transformations de calque ( `crop=`, `scale=`, `rotate=`, `flip=`) appliquées à la source du calque. Overrides `anchor=`. Ignoré par les calques d’effet.

## Par défaut {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Si ce n’ `origin=` est pas le cas, le calque   est déterminé en appliquant le calque à l’ancre de l’image. Si l’ancrage de l’image n’est pas connu, le centre du rectangle du calque ( `originN=0,0`) est utilisé.

## Exemple {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Voir Exemple A dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [extended=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
