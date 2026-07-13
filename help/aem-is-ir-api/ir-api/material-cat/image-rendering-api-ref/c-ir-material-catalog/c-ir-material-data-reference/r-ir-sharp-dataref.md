---
description: 'Accentuation. Attribut Accentuation : détermine à quel moment la matière est accentuée lors du rendu.'
solution: Experience Manager
title: Sharp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
TQID: 'https://experienceleague.adobe.com/e9pUY-R7wpieviEUxzGeuyGduEKTLGf4cZz57Kc2Qhs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 8%

---

# Sharp{#sharp}

Accentuation. Attribut Accentuation : détermine à quel moment la matière est accentuée lors du rendu.

Le type et l’intensité de l’accentuation sont contrôlés par la vignette au moyen d’un modèle de matériau par défaut ou avec des `catalog::RenderSettings`.

## Propriétés {#section-aac81b1a611b4bca90b8544eae7896df}

Énumération.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Aucun accentuation. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Accentuation normale (après la transformation). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Accentuation alternative (avant la transformation). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Accentuation supplémentaire (avant et après la transformation). </p></td> 
 </tr> 
</table>

Ignoré par les matériaux de couleur unie, facultatif pour tous les autres matériaux.

## Par défaut {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` est utilisé si le champ n’est pas présent, s’il est vide ou si la valeur ne fait pas partie des choix pris en charge.

## Voir aussi {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribute::Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)

