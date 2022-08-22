---
title: Sharp
description: Accentuation des matériaux par défaut. Définit le mode d’accentuation des matériaux par défaut lorsqu’un enregistrement de catalogue particulier ne contient pas de valeur d’accentuation de catalogue valide.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 11%

---

# Sharp{#sharp}

Accentuation des matériaux par défaut. Définit le mode d’accentuation des matériaux par défaut au cas où un enregistrement de catalogue particulier ne contiendrait pas un enregistrement valide `catalog::Sharp` .

## Propriétés {#section-dcb810d01b8a40eb991d555a3cbe48b9}

Enum.

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
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
  <td class="stentry"> <p>Accentuation (avant et après la transformation). </p> </td> 
 </tr> 
</table>

## Par défaut {#section-613130fca7c04ce7a7734265f27aa1ea}

Hérité de `default::Sharp` s’il n’est pas défini ou s’il est vide.

## Voir aussi {#section-7771824f2822443ab0297e8793bb48ae}

[catalogue : Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a), [catalogue ::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
