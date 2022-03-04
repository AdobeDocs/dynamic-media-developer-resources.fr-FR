---
title: Valeurs de couleur
description: Les valeurs de couleur des attributs color= et bgc= peuvent être spécifiées à l’aide d’une liste de valeurs de composant décimales séparées par des virgules ou d’une notation hexadécimale, similaire au HTML.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 608ff0f1-4fbd-4e32-af07-3a62569d14c7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 13%

---

# Valeurs de couleur{#color-values}

Valeurs de couleur pour `color=` et `bgc=` Les attributs peuvent être spécifiés à l’aide d’une liste de valeurs de composant séparées par des virgules ou d’une notation hexadécimale, similaire à un HTML.

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> color</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{ {red, green, blue} | gray } | { [ 0x ] hex6 } | { 0xhex2 }</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>rouge, vert, bleu, gris</i> </p></td> 
  <td class="stentry"> <p>Valeur du composant de couleur (0...255, nombre entier décimal). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex6</i> </p></td> 
  <td class="stentry"> <p>Valeur de couleur du RGB hexadécimal à six chiffres (RRGBB) prise en charge. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex2</i> </p></td> 
  <td class="stentry"> <p>Valeur de couleur hexadécimale grise à deux chiffres (0...FF) compressée. </p></td> 
 </tr> 
</table>

## Exemples {#section-a78732151d584e84abeb99f9ce8d7c24}

Voici quelques exemples de paramètres de couleurs valides et leur interprétation de valeur de couleur de RGB correspondante :

<table id="simpletable_837B3173020240A5B7B2DB2F4CC57352"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 100 200 </p></td> 
  <td class="stentry"> <p>(0,100,200) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>128 </p></td> 
  <td class="stentry"> <p>(128 128 128) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0x010203 </p></td> 
  <td class="stentry"> <p>(1,2,3) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>00b1c2 </p></td> 
  <td class="stentry"> <p>(160 177 194) </p></td> 
 </tr> 
</table>

## Voir aussi {#section-207d5cb918a94736a27445faa58917d3}

[color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa), [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0), [grout=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
