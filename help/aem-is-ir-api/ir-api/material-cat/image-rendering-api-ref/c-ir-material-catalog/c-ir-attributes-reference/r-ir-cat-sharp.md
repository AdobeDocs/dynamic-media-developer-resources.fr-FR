---
title: Sharp
description: Accentuation par défaut du matériau. Définit le mode d’accentuation de matériau par défaut au cas où un enregistrement de catalogue spécifique ne contiendrait aucune valeur d’accentuation de catalogue valide.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
TQID: 'https://experienceleague.adobe.com/BUhpguI3knVzevI-ymAt4Xz-faYKbXgHMXW0O9Mf8oo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 88
ht-degree: 10%

---

# Sharp{#sharp}

Accentuation par défaut du matériau. Définit le mode d’accentuation de matériau par défaut au cas où un enregistrement de catalogue spécifique ne contiendrait aucune valeur de `catalog::Sharp` valide.

## Propriétés {#section-dcb810d01b8a40eb991d555a3cbe48b9}

Énumération.

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
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
  <td class="stentry"> <p>Accentuation supplémentaire (avant et après la transformation). </p> </td> 
 </tr> 
</table>

## Par défaut {#section-613130fca7c04ce7a7734265f27aa1ea}

Hérité de `default::Sharp` si non défini ou si vide.

## Voir aussi {#section-7771824f2822443ab0297e8793bb48ae}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a), [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
