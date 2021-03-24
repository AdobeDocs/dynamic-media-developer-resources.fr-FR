---
description: Affiche les repères d’impression. Indique comment afficher les repères d’impression.
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 30%

---


# printerMark{#printermark}

Affiche les repères d’impression. Indique comment afficher les repères d’impression.

` printerMark= *`trim `*, *`marksbleed `*, *`marksenregistrement `*, *`markscolor `*, *`barspage information `*, *``*, *`styleline `*, *`pestlayer intégré`*`

Les différentes marques peuvent être désactivées ou désactivées. Le style des repères d’impression peut également être contrôlé.

Les valeurs valides sont les suivantes :

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>trim marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Valeur par défaut : 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>bleed marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Valeur par défaut : 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>registration marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Valeur par défaut : 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>color bars= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Valeur par défaut : 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page information= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Valeur par défaut : 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Par défaut </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>Par défaut : Par défaut </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>poids de ligne= </p></td> 
  <td class="stentry"> <p>Toute valeur comprise entre 0,125 et 2,0. </p></td> 
  <td class="stentry"> <p>Valeur par défaut : 0.25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Valeur par défaut : 1. </p></td> 
 </tr> 
</table>

## Exemple {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
