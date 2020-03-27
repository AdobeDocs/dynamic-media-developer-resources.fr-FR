---
description: Attributs de texte sur chemin.
seo-description: Attributs de texte sur chemin.
seo-title: pathAttr
solution: Experience Manager
title: pathAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b0ca5821-ee08-4c18-919d-775b75f19acd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pathAttr{#pathattr}

Attributs de texte sur chemin.

` pathAttr= *``*[, *``*[, *`directionstartPosendPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> direction </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norme </span> | <span class="codeph"> inversé </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>Position du de texte sur le chemin d’accès (réel 0.0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>Position de fin du texte sur le chemin (réel 0.0...&lt;2.0). </p> </td> 
 </tr> 
</table>

Spécifiez `norm` pour dessiner le texte en commençant près du premier sommet du tracé et `reverse` pour dessiner le texte dans la direction opposée, en commençant près du dernier sommet.

*`startPos`* et *`endPos`* permettre d&#39;ajuster où le texte sera tracé sur le chemin. 0,0 correspond au premier sommet du chemin et 1,0 au dernier sommet ; les valeurs intermédiaires expriment la distance le long du chemin entre le premier et le dernier sommet.

## Propriétés {#section-80f266da4e2549d89f022a3f9ff4584d}

Attribut de calque. Ignoré si le calque n’inclut pas `textPs=` de commandes et `textPath=` de commandes.

*`startPos`* doit être supérieur ou égal à 0 et inférieur à 1.0. *`endPos`* doit être supérieur *`startPos`* et inférieur ou égal à 1,0 lorsqu&#39;il est appliqué à un chemin ouvert, ou inférieur ou égal à ( *`startPos`* + 1,0) lorsqu&#39;il est appliqué à un chemin fermé.

## Par défaut {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Voir aussi {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
