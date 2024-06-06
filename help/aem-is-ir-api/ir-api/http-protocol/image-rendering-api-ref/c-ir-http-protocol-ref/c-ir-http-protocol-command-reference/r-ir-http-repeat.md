---
title: répéter
description: Mode de répétition de la texture. Spécifie le mode de répétition pour les matériaux de texture répétables.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6cc82742-4ba0-4524-a87b-586539d7fe38
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 16%

---

# répéter{#repeat}

Mode de répétition de la texture. Spécifie le mode de répétition pour les matériaux de texture répétables.

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p> </td> 
  <td class="stentry"> <p>Répétez immédiatement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Carrelage aléatoire à 4 voies. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Carrelage aléatoire à 8 voies. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Carrelage en diamant. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Un papier peint à 1/4 goutte suspendu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Papier peint de troisième dépôt suspendu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>Un papier peint à demi-goutte suspendu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>Papier peint de la cinquième goutte suspendu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>Papier peint inversé suspendu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>Papier peint aléatoire suspendu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p> </td> 
  <td class="stentry"> <p>Abandon aléatoire. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p> </td> 
  <td class="stentry"> <p>Aléatoire. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p> </td> 
  <td class="stentry"> <p>La moitié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p> </td> 
  <td class="stentry"> <p>Miroir (correspondance de livre). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p> </td> 
  <td class="stentry"> <p>Optimiseur aléatoire standard. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p> </td> 
  <td class="stentry"> <p>Optimiseur aléatoire haute fréquence. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p> </td> 
  <td class="stentry"> <p>aléisseur de basse fréquence. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p> </td> 
  <td class="stentry"> <p>Opérateur aléatoire horizontal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p> </td> 
  <td class="stentry"> <p>Optimiseur vertical. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p> </td> 
  <td class="stentry"> <p>Optimiseur de périphérie. </p> </td> 
 </tr> 
</table>

Les modes de mise en forme aléatoire (14...18) peuvent être utilisés pour synthétiser les textures à partir d’images qui ne sont pas facilement répétables ; l’algorithme crée des textures complètement aléatoires ou partiellement aléatoires basées sur l’image d’origine.

## Propriétés {#section-262bf540930d4890b678ea00cefe1909}

Attribut de matière. Ignoré par les matériaux couleur unie, décal et armoire.

## Par défaut {#section-e5bbd7d9fbb74852849e605d20f550bb}

`catalog::Repeat`, si le matériau est basé sur une entrée de catalogue, sinon `0` (répétition droite).

## Voir aussi {#section-ac99113b64654d75a3a86e41db546269}

[catalogue : Répéter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)
