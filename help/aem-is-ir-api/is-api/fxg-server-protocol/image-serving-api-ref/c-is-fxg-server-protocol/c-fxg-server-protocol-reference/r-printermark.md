---
description: Affiche les repères d’impression. Indique comment afficher les repères d’impression.
seo-description: Affiche les repères d’impression. Indique comment afficher les repères d’impression.
seo-title: printerMark
solution: Experience Manager
title: printerMark
topic: Scene7 Image Serving - Image Rendering API
uuid: 3e5699ce-3ccd-4f85-91dd-c40c252a758d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# printerMark{#printermark}

Affiche les repères d’impression. Indique comment afficher les repères d’impression.

` printerMark= *`trim`*, *`marqusbleed`*, *`marksenregistrement`*, *`markscolor`*, *`barspage`*, *``*, *`informationstyleline`*, *`pestlayer intégré`*`

Les différents repères peuvent être désactivés ou activés. Le style des repères d’impression peut également être contrôlé.

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
  <td class="stentry"> <p>La valeur par défaut est Default </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>de ligne = </p></td> 
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
