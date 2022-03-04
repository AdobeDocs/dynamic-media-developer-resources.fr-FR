---
description: Attributs de texte sur chemin.
solution: Experience Manager
title: pathAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---

# pathAttr{#pathattr}

Attributs de texte sur chemin.

` pathAttr= *`direction`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> direction </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> standard </span> | <span class="codeph"> reverse </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>Position de départ du texte sur le chemin (réel 0.0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>Position de fin du texte sur le chemin (réel 0.0...&lt;2.0). </p> </td> 
 </tr> 
</table>

Spécifier `norm` pour tracer du texte à proximité du premier sommet du chemin et `reverse` pour tracer le texte dans la direction opposée, en commençant près du dernier sommet.

*`startPos`* et *`endPos`* permettent d’ajuster l’emplacement du texte dessiné sur le chemin. 0.0 correspond au premier sommet du chemin et 1.0 au dernier sommet ; les valeurs intermédiaires expriment la distance le long du chemin entre le premier et le dernier sommet.

## Propriétés {#section-80f266da4e2549d89f022a3f9ff4584d}

Attribut de calque. Ignoré si le calque n’inclut pas `textPs=` et `textPath=` des commandes.

*`startPos`* doit être supérieur ou égal à 0 et inférieur à 1.0. *`endPos`* doit être supérieur à *`startPos`* et inférieur ou égal à 1,0 lorsqu’il est appliqué à un chemin d’accès ouvert ou inférieur ou égal à ( *`startPos`* + 1.0) lorsqu’il est appliqué à un chemin fermé.

## Par défaut {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Voir aussi {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
