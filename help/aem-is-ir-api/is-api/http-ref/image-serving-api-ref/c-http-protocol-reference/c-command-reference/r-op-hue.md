---
title: op_hue
description: Règle la teinte de l’image. Décale la teinte de chaque pixel visible du calque ou de l’image composite de la quantité spécifiée.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
TQID: 'https://experienceleague.adobe.com/6VSkHDcXsf531qB6okDvLt-xIyFoiw-fG3Z11a-Ne5g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 1%

---

# op_hue{#op-hue}

Règle la teinte de l’image. Décale la teinte de chaque pixel visible du calque ou de l’image composite de la quantité spécifiée.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Réglage de la teinte en degrés (-180...+180 int). </p></td> 
 </tr> 
</table>

Sur la base d’une plage de teintes à 360 degrés.

## Propriétés {#section-55779644700b4c808a624cdf5a04447e}

Commande Calque. S’applique au calque actif ou à l’image composite, le cas `layer=comp`. Ignoré par les calques d’effet. Les images ou calques CMJN sont convertis en RGB avant l’application de l’opération.

## Par défaut {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, pour aucun changement de teinte.
