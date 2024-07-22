---
description: Afficher les repères d’impression. Indique le mode d’affichage des repères d’impression.
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 18%

---

# printerMark{#printermark}

Afficher les repères d’impression. Indique le mode d’affichage des repères d’impression.

` printerMark= *`marques de rognage`*, *`marques de rognage`*, *`marques d’enregistrement`*, *`barres de couleurs`*, *`informations sur la page`*, *`style`*, *`poids de ligne`*, *`élément de calque `*`

Les différentes marques peuvent être désactivées. Le style des marques de l’imprimante peut également être contrôlé.

Les valeurs valides sont les suivantes :

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>trim marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Par défaut : 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>bleed marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Par défaut : 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>marques d’enregistrement= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Par défaut : 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>color bars= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Par défaut : 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page information= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Par défaut : 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Par défaut </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>La valeur par défaut est </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>line weight= </p></td> 
  <td class="stentry"> <p>Toute valeur comprise entre 0,125 et 2,0 inclut les deux valeurs. </p></td> 
  <td class="stentry"> <p>Par défaut : 0,25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Par défaut : 1. </p></td> 
 </tr> 
</table>

## Exemple {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
