---
description: Ajustez la couleur. Permet de changer la teinte de chaque pixel visible du calque ou de l’image composite selon la quantité spécifiée.
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# op_hue{#op-hue}

Ajustez la couleur. Permet de changer la teinte de chaque pixel visible du calque ou de l’image composite selon la quantité spécifiée.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajustement des nuances en degrés (-180...+180 int). </p></td> 
 </tr> 
</table>

Basée sur une plage de 360 degrés.

## Propriétés {#section-55779644700b4c808a624cdf5a04447e}

Couche, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet. Les images ou calques CMJN sont convertis en RVB avant l’application de l’opération.

## Par défaut {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, pour aucun changement de couleur.
