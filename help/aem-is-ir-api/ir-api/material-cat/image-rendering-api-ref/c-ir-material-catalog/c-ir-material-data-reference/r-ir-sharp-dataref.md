---
description: Accentuation. Attribut d’accentuation qui détermine le moment où le matériau est accentué au cours du rendu.
solution: Experience Manager
title: Sharp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 8%

---

# Sharp{#sharp}

Accentuation. Attribut d’accentuation qui détermine le moment où le matériau est accentué au cours du rendu.

Le type et la quantité d’accentuation sont contrôlés par la vignette au moyen d’un modèle de matériau par défaut ou avec `catalog::RenderSettings`.

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
  <td class="stentry"> <p>Autre accentuation (avant la transformation). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Plus d’accentuation (avant et après la transformation). </p></td> 
 </tr> 
</table>

Ignoré par les matériaux couleur solides, facultatif pour tous les autres matériaux.

## Par défaut {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` est utilisé si le champ est absent, s’il est vide ou si la valeur n’est pas l’un des choix pris en charge.

## Voir aussi {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribute::Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
