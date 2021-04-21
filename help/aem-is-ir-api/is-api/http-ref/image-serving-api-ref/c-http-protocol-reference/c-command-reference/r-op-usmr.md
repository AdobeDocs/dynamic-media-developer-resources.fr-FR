---
description: Masque flou. L’accentuation masque le calque ou l’image de vue finale, après mise à l’échelle, si layer=comp.
solution: Experience Manager
title: op_usmR
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---


# op_usmR{#op-usmr}

Masque flou. L’accentuation masque le calque ou l’image de vue finale, après mise à l’échelle, si layer=comp.

Les paramètres sont appliqués en l’état, que l’échantillonnage en aval ait été effectué ou non.

`op_usmR= *``*[, *``*[, *``*[, *`montant tradiusRbattholdmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> montant</span></span> </p></td> 
  <td class="stentry"> <p>Facteur de résistance du filtre (réel 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>Rayon du noyau du filtre en pixels (réel 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> seuil</span></span> </p></td> 
  <td class="stentry"> <p>Niveau de seuil du filtre (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monochrome</span></span> </p></td> 
  <td class="stentry"> <p>Définissez sur 0 pour appliquer séparément chaque composante de couleur ou sur 1 pour appliquer uniquement la luminosité de l’image (intensité). </p> <p><span class="codeph"> <span class="varname"> Les images </span></span> monochromes sont ignorées pour les images en niveaux de gris. </p> </td> 
 </tr> 
</table>

Le masque de calque ou le masque composite est également accentué.

## Propriétés {#section-fb5311b34d164946b74dadb32359518a}

Attribut de couche ou attribut de vue. S’applique au calque actif ou à l’image de vue finale si `layer=comp`. Les calques d’effets l’ignorent.

## Par défaut {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` sans effet de masquage flou.

## Voir aussi {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
