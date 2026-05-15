---
title: pathAttr
description: Attributs de texte sur chemin.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
TQID: 'https://experienceleague.adobe.com/A7uOgsYtOH6AmVOtbUfQDVJHwJEkCSXqBYavY9CbRkw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 1%

---

# pathAttr{#pathattr}

Attributs de texte sur chemin.

` pathAttr= *`direction`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de direction <span class="varname"> </p> </td> 
  <td class="stentry"> <p> </span> de la norme <span class="codeph"> | </span> inverse <span class="codeph"> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>Position de début du texte sur le chemin (0,0...1,0 réel). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>Position de fin du texte sur le chemin (réel 0,0...&lt;2,0). </p> </td> 
 </tr> 
</table>

Indiquez `norm` dessiner du texte commençant près du premier sommet de tracé et `reverse` pour dessiner du texte dans la direction opposée, commençant près du dernier sommet.

*`startPos`* et *`endPos`* permettent d’ajuster l’emplacement du texte sur le tracé. 0,0 correspond au premier sommet de la trajectoire et 1,0 au dernier sommet ; les valeurs intermédiaires expriment la distance le long de la trajectoire entre le premier et le dernier sommet.

## Propriétés {#section-80f266da4e2549d89f022a3f9ff4584d}

Attribut de calque. Ignoré si le calque n’inclut pas les commandes `textPs=` et `textPath=`.

*`startPos`* doit être supérieur ou égal à 0 et inférieur à 1,0. *`endPos`* doit être supérieur à *`startPos`* et inférieur ou égal à 1,0 lorsqu’il est appliqué à un chemin ouvert, ou inférieur ou égal à ( *`startPos`* + 1,0) lorsqu’il est appliqué à un chemin fermé.

## Par défaut {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Voir aussi {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
