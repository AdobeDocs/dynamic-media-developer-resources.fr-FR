---
title: recadrer
description: Recadrer l’image. Indique une zone de recadrage rectangulaire, exprimée en pixels ou normalisée par rapport à l’image source ou à l’image de masque en pleine résolution.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
TQID: 'https://experienceleague.adobe.com/sFmHyBwHZcqIxp9LWE8IphN3RCa-auGEph0WbFzs1n0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 1%

---

# recadrer{#crop}

Recadrer l’image. Indique une zone de recadrage rectangulaire, exprimée en pixels ou normalisée par rapport à l’image source ou à l’image de masque en pleine résolution.

`crop= *`coord`*, *`size`*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>Décalage en pixels entre le coin supérieur gauche de l’image source et le coin supérieur gauche du recadrage (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Décalage normalisé entre le coin supérieur gauche de l’image source et le coin supérieur gauche du recadrage (réel, réel). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> taille</span></span> </p></td> 
  <td class="stentry"> <p>Taille du recadrage en pixels (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>La taille normalisée du recadrage est relative à la taille de l’image source (réelle, réelle). </p></td> 
 </tr> 
</table>

Peut également être utilisé pour étendre l’image au-delà de ses limites en spécifiant des valeurs négatives x, y et/ou des valeurs de largeur et de hauteur plus grandes que la largeur et la hauteur de l’image. Dans ce cas, la zone étendue est entièrement transparente (sauf si `bgColor=` est spécifié).

## Propriétés {#section-632e0405bb9940679b5f8b1c10e0902e}

Attribut image/mask Source. S&#39;applique à l&#39;image source du calque 0 si `layer=comp`. Ignoré par les calques qui ne sont pas associés à une image ou un masque source.

## Par défaut {#section-41f62d386c664f77952bc22e7286bb88}

Image entière ( `cropN=0,0,1,1`).

## Exemples {#section-2c99b481c0a04321979a3b522aa295d1}

**Recadrez 10 % de la gauche et 10 % de la droite :**

`…&cropN=0.1,0,0.8,1&…`

**Recadrez 20 % du bord inférieur d’une image :**

`…&cropN=0,0,1,0.8&…`

## Voir aussi {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropsPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
