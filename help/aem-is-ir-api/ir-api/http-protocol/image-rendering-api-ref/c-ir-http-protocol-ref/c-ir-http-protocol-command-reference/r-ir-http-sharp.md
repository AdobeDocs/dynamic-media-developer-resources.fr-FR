---
title: sharp
description: Accentuer la texture. Spécifie l’accentuation à appliquer lors du rendu de ce matériau.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 5%

---

# sharp{#sharp}

Accentuer la texture. Spécifie l’accentuation à appliquer lors du rendu de ce matériau.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p> </td> 
  <td class="stentry"> <p>Aucune accentuation. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Accentuation normale (en retard). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 accentuation alternative (tôt). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Plus d’accentuation (tôt et tard). </p> </td> 
 </tr> 
</table>

`sharp=1` Applique l’accentuation après le rendu de la matière. `sharp=2` applique l’accentuation après le redimensionnement initial de la texture, mais avant sa transformation en scène. `sharp=3` applique l’accentuation avant et après la transformation.

L’algorithme d’accentuation et la quantité d’accentuation et les autres paramètres USM (masquage flou) sont contrôlés par le modèle de matériau par défaut fourni par la vignette ou avec `rs=`.

## Propriétés {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Attribut de matière. Ignoré par les matériaux couleur solides.

## Par défaut {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, si la matière est basée sur une entrée de catalogue, sinon `attribute::Sharp`.

## Voir aussi {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
