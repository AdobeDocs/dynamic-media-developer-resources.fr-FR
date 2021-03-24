---
description: Accentuation. Attribut d’accentuation, détermine le moment où le matériau est accentué pendant le rendu.
solution: Experience Manager
title: Sharp
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 10%

---


# Net{#sharp}

Accentuation. Attribut d’accentuation, détermine le moment où le matériau est accentué pendant le rendu.

Le type et la quantité d’accentuation sont contrôlés par la vignette via un modèle de matériau par défaut ou avec `catalog::RenderSettings`.

## Propriétés {#section-aac81b1a611b4bca90b8544eae7896df}

Enum.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p></td> 
  <td class="stentry"> <p>Aucune accentuation. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Accentuation normale (après la transformation). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Accentuation secondaire (avant la transformation). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Accentuation (avant et après la transformation). </p></td> 
 </tr> 
</table>

Ignoré par les matériaux de couleur unie, facultatif pour tous les autres matériaux.

## Par défaut {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` est utilisée si le champ n’est pas présent, s’il est vide ou si la valeur n’est pas l’un des choix pris en charge.

## Voir aussi {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribut ::Accentuation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) ,  [catalogue::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd),  [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
