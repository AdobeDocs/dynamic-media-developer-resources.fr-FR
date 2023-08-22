---
title: op_colorbalance
description: Ajuster l’équilibre des couleurs. Ajuste séparément la valeur de chaque composant de couleur de RGB.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 1%

---

# op_colorbalance{#op-colorbalance}

Ajuster l’équilibre des couleurs. Ajuste séparément la valeur de chaque composant de couleur de RGB.

`op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Ajustement des composants rouges (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Ajustement des composants verts (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Ajustement des composants bleus (-100...+100 int). </p></td> 
 </tr> 
</table>

Les données d’image d’entrée en gris et CMJN sont converties en RGB à l’aide d’une conversion naïve, qui n’est pas exacte lorsque la gestion des couleurs est activée.

## Propriétés {#section-dff9c934f7c1442bbd02379b688d82e2}

Couche, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet. Les images et calques CMJN sont convertis en RGB avant l’application de l’opération.

## Par défaut {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` pour aucun changement de couleur.

## Exemple {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Poussez la balance des couleurs vers le rouge :

… `&op_colorBalance=100,0,0&`…
