---
description: Ajuster la teinte. Déplace la teinte de chaque pixel visible du calque ou de l’image composite selon la valeur indiquée.
seo-description: Ajuster la teinte. Déplace la teinte de chaque pixel visible du calque ou de l’image composite selon la valeur indiquée.
seo-title: op_hue
solution: Experience Manager
title: op_hue
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 23da539e-0192-4dc4-a19b-41aa94a82730
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

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
