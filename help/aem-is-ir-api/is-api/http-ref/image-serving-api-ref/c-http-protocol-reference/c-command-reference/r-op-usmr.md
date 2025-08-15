---
title: op_usmR
description: Accentuation. L’accentuation masque le calque ou l’image d’affichage final, après mise à l’échelle, si calque=terminé.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# op_usmR{#op-usmr}

Accentuation. L’accentuation masque le calque ou l’image d’affichage final, après mise à l’échelle, si calque=terminé.

Les paramètres sont appliqués tels quels, qu’il y ait eu ou non sous-échantillonnage.

`op_usmR= *`amount`*[, *`radiusR`*[, *`threshold`*[, *`monochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> montant</span></span> </p></td> 
  <td class="stentry"> <p>Facteur de résistance du filtre (0...5 réel). </p></td> 
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
  <td class="stentry"> <p>Définissez cette valeur sur 0 pour appliquer séparément chaque composante de couleur ou sur 1 pour appliquer uniquement la luminosité (intensité) de l’image. </p> <p><span class="codeph"> <span class="varname"> monochrome</span></span> est ignoré pour les images en niveaux de gris. </p> </td> 
 </tr> 
</table>

Le masque de calque ou composite est également accentué.

## Propriétés {#section-fb5311b34d164946b74dadb32359518a}

Attribut de calque ou attribut de vue. S’applique au calque actif ou à l’image d’affichage final, le cas `layer=comp`. Les calques d’effet l’ignorent.

## Par défaut {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` pour l’absence d’effet d’accentuation.

## Voir aussi {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
