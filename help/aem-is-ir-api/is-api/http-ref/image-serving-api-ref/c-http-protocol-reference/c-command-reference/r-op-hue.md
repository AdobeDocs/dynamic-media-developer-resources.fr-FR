---
description: Ajuster la teinte. Déplace la teinte de chaque pixel visible du calque ou de l’image composite selon la valeur indiquée.
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 2%

---


# op_hue{#op-hue}

Ajuster la teinte. Déplace la teinte de chaque pixel visible du calque ou de l’image composite selon la valeur indiquée.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Réglage de la teinte en degrés (-180...+180 int). </p></td> 
 </tr> 
</table>

Basé sur une gamme de teintes de 360 degrés.

## Propriétés {#section-55779644700b4c808a624cdf5a04447e}

Calque, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet. Les images ou calques CMJN sont convertis en RVB avant l’application de l’opération.

## Par défaut {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, sans changement de teinte.
