---
description: Recadrer l’image. Indique une zone de recadrage rectangulaire, exprimée en pixels ou normalisée par rapport à l’image source ou de masque à résolution totale.
solution: Experience Manager
title: Recadrer
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---


# Recadrer{#crop}

Recadrer l’image. Indique une zone de recadrage rectangulaire, exprimée en pixels ou normalisée par rapport à l’image source ou de masque à résolution totale.

`crop= *``*, *`coordsize`*`

`cropN= *``*, *`coordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>Décalage en pixels du coin supérieur gauche de l’image source vers le coin supérieur gauche de la recette de recadrage (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Décalage normalisé depuis le coin supérieur gauche de l’image source vers le coin supérieur gauche du rectangle de recadrage (réel, réel). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> taille</span></span> </p></td> 
  <td class="stentry"> <p>Taille du rectangle de recadrage en pixels (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Taille normalisée de la recette de recadrage par rapport à la taille de l’image source (réelle, réelle). </p></td> 
 </tr> 
</table>

Peut également être utilisé pour étendre l’image au-delà de ses limites en spécifiant des valeurs négatives x, y et/ou width, des valeurs de hauteur supérieures à la largeur et la hauteur de l’image. Dans ce cas, la zone étendue est entièrement transparente (sauf si `bgColor=` est spécifié).

## Propriétés {#section-632e0405bb9940679b5f8b1c10e0902e}

Attribut image/masque source. S’applique à l’image source du calque 0 si `layer=comp`. Ignoré par les calques qui ne sont pas associés à une image ou à un masque source.

## Par défaut {#section-41f62d386c664f77952bc22e7286bb88}

Image entière ( `cropN=0,0,1,1`).

## Exemples {#section-2c99b481c0a04321979a3b522aa295d1}

**Recadrer 10 % sur la gauche et 10 % sur la droite :**

`…&cropN=0.1,0,0.8,1&…`

**Recadrer de 20 % le bord inférieur d’une image :**

`…&cropN=0,0,1,0.8&…`

## Voir aussi {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [culturePathColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c),  [extended=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
