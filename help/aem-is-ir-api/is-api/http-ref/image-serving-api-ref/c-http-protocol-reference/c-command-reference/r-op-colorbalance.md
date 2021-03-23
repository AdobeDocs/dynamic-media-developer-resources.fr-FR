---
description: Réglage de l’équilibre des couleurs. Ajuste séparément la valeur de chaque composante de couleur RVB.
seo-description: Réglage de l’équilibre des couleurs. Ajuste séparément la valeur de chaque composante de couleur RVB.
seo-title: op_colorbalance
solution: Experience Manager
title: op_colorbalance
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# op_colorbalance{#op-colorbalance}

Réglage de l’équilibre des couleurs. Ajuste séparément la valeur de chaque composante de couleur RVB.

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Réglage des composantes rouges (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Réglage des composantes vertes (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Réglage des composantes bleues (-100...+100 int). </p></td> 
 </tr> 
</table>

Les données d’image d’entrée en gris et CMJN sont converties en RVB à l’aide d’une conversion naïve, ce qui n’est pas exact lorsque la gestion des couleurs est activée.

## Propriétés {#section-dff9c934f7c1442bbd02379b688d82e2}

Calque, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet. Les images et calques CMJN sont convertis en RVB avant l’application de l’opération.

## Par défaut {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` sans changement de couleur.

## Exemple {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Poussez la balance des couleurs vers le rouge :

... `&op_colorBalance=100,0,0&`...
