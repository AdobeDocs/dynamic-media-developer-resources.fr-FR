---
description: Masque flou. L’accentuation masque le calque ou l’image finale du, après tout le redimensionnement, si layer=comp.
seo-description: Masque flou. L’accentuation masque le calque ou l’image finale du, après tout le redimensionnement, si layer=comp.
seo-title: op_usm
solution: Experience Manager
title: op_usm
topic: Scene7 Image Serving - Image Rendering API
uuid: c647e063-2405-489b-b14d-a70638ac8af7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_usm{#op-usm}

Masque flou. L’accentuation masque le calque ou l’image finale du, après tout le redimensionnement, si layer=comp.

Les paramètres sont supposés s’appliquer à l’image à résolution entière et sont réduits lors du traitement d’une image sous-échantillonnée.

`op_usm= *``*[, *``*[, *``*[, *`montant tradiusbattholdmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> montant</span></span> </p></td> 
  <td class="stentry"> <p>Facteur de résistance du filtre (réel 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p></td> 
  <td class="stentry"> <p>Rayon du noyau du filtre en pixels (réel 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> seuil</span></span> </p></td> 
  <td class="stentry"> <p>Niveau de seuil du filtre (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monochrome</span></span> </p></td> 
  <td class="stentry"> <p>Définissez sur 0 pour appliquer séparément chaque composante de couleur ou sur 1 pour appliquer uniquement à la luminosité (intensité) de l’image. </p> <p> <span class="codeph"><span class="varname"> monochrome</span></span> est ignoré pour les images en niveaux de gris. </p></td> 
 </tr> 
</table>

Le masque de fusion ou le masque composite est également accentué.

## Propriétés {#section-fb5311b34d164946b74dadb32359518a}

Attribut de calque ou attribut de  de. S’applique au calque actif ou à l’image de  finale du, le cas échéant `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` sans effet de masquage flou.

## Voir aussi {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
