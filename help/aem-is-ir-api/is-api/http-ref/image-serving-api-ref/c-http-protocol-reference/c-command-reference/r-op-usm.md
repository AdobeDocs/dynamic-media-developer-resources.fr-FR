---
title: op_usm
description: Accentuation. L’accentuation masque le calque ou l’image d’affichage final, après mise à l’échelle, si calque=terminé.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
TQID: 'https://experienceleague.adobe.com/Q2-9E1SNDgr8rGYWNKDLlVcQU85EhpEXhxAqF3WrJic'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 1%

---

# op_usm{#op-usm}

Accentuation. L’accentuation masque le calque ou l’image d’affichage final, après mise à l’échelle, si calque=terminé.

Les paramètres sont supposés s’appliquer à l’image en pleine résolution et sont réduits lors du traitement d’une image sous-échantillonnée.

`op_usm= *`amount`*[, *`radius`*[, *`threshold`*[, *`monochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> montant</span></span> </p></td> 
  <td class="stentry"> <p>Facteur de résistance du filtre (0...5 réel). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> rayon </span></span> </p></td> 
  <td class="stentry"> <p>Rayon du noyau du filtre en pixels (réel 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> seuil</span></span> </p></td> 
  <td class="stentry"> <p>Niveau de seuil du filtre (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monochrome</span></span> </p></td> 
  <td class="stentry"> <p>Définissez cette valeur sur 0 pour appliquer séparément chaque composante de couleur ou sur 1 pour appliquer uniquement la luminosité (intensité) de l’image. </p> <p> <span class="codeph"><span class="varname"> monochrome</span></span> est ignoré pour les images en niveaux de gris. </p></td> 
 </tr> 
</table>

Le masque de calque ou composite est également accentué.

## Propriétés {#section-fb5311b34d164946b74dadb32359518a}

Attribut de calque ou attribut de vue. S’applique au calque actif ou à l’image d’affichage final, le cas `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` pour l’absence d’effet d’accentuation.

## Voir aussi {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
