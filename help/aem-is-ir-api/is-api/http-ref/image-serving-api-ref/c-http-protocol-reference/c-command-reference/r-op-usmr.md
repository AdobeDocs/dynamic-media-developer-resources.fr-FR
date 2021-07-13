---
description: Masquage flou. L’accentuation masque le calque ou l’image d’affichage final, après toute mise à l’échelle, si layer=comp.
solution: Experience Manager
title: op_usmR
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 4%

---

# op_usmR{#op-usmr}

Masquage flou. L’accentuation masque le calque ou l’image d’affichage final, après toute mise à l’échelle, si layer=comp.

Les paramètres sont appliqués tels quels, qu’un échantillonnage ait été effectué ou non.

`op_usmR= *``*[, *``*[, *``*[, *`amount tradiusRbattholdmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> montant</span></span> </p></td> 
  <td class="stentry"> <p>Facteur de résistance du filtre (réel 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>Filtrez le rayon du noyau en pixels (réel 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> seuil</span></span> </p></td> 
  <td class="stentry"> <p>Niveau de seuil du filtre (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monochrome</span></span> </p></td> 
  <td class="stentry"> <p>Définissez cette variable sur 0 pour l’appliquer séparément à chaque composant de couleur ou sur 1 pour l’appliquer uniquement à la luminosité de l’image (intensité). </p> <p><span class="codeph"> <span class="varname"> Les monochromes </span></span>  sont ignorées pour les images en niveaux de gris. </p> </td> 
 </tr> 
</table>

Le masque de calque ou le masque composite est également accentué.

## Propriétés {#section-fb5311b34d164946b74dadb32359518a}

Attribut de calque ou attribut d’affichage. S’applique au calque actif ou à l’image de vue finale si `layer=comp`. Les calques d’effet l’ignorent.

## Par défaut {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` sans effet de masquage flou.

## Voir aussi {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
