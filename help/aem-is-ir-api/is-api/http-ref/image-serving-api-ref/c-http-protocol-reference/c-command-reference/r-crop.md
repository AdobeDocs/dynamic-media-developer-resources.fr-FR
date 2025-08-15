---
title: jabot
description: Recadrer l’image. Spécifie une zone de recadrage rectangulaire, exprimée en pixels ou normalisée par rapport à l’image source pleine résolution ou à l’image de masque.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# jabot{#crop}

Recadrer l’image. Spécifie une zone de recadrage rectangulaire, exprimée en pixels ou normalisée par rapport à l’image source pleine résolution ou à l’image de masque.

`crop= *`Taille du coord`*, *` `*`

`cropN= *`coordN`*, *`tailleN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>Décalage des pixels entre le coin supérieur gauche de l’image source et le coin supérieur gauche du rect de recadrage (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Décalage normalisé du coin supérieur gauche de l’image source vers le coin supérieur gauche du rect de recadrage (réel, réel). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> taille</span></span> </p></td> 
  <td class="stentry"> <p>Taille du rect de recadrage en pixels (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> tailleN</span></span> </p></td> 
  <td class="stentry"> <p>Taille normalisée du rect de recadrage par rapport à la taille de l’image source (réelle, réelle). </p></td> 
 </tr> 
</table>

Peut également être utilisé pour étendre l’image au-delà de ses limites en spécifiant des valeurs négatives x, y et / ou largeur, des valeurs de hauteur supérieures à la largeur de l’image, hauteur. Dans ce cas, la zone étendue est entièrement transparente (sauf `bgColor=` indication contraire).

## Propriétés {#section-632e0405bb9940679b5f8b1c10e0902e}

Attribut image source/masque. S’applique à l’image source du calque 0 si `layer=comp`. Ignoré par les calques qui ne sont pas associés à une image source ou à un masque.

## Par défaut {#section-41f62d386c664f77952bc22e7286bb88}

Image entière ( `cropN=0,0,1,1`).

## Exemples {#section-2c99b481c0a04321979a3b522aa295d1}

**Recadrage de 10 % sur la gauche et de 10 % sur la droite :**

`…&cropN=0.1,0,0.8,1&…`

**Recadrage de 20 % du bord inférieur d’une image :**

`…&cropN=0,0,1,0.8&…`

## Voir aussi {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
