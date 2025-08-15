---
title: scl
description: Vue d’échelle. Met à l’échelle l’image rendue selon le facteur d’échelle spécifié par rapport à la vignette pleine résolution.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---

# scl{#scl}

Vue d’échelle. Met à l’échelle l’image rendue selon le facteur d’échelle spécifié par rapport à la vignette pleine résolution.

`scl= *`Facteur invTarget`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Facteur invTarget</span> </span> </p></td> 
  <td class="stentry"> <p>Facteur d’échelle inverse (réel, supérieur ou égal à 1,0). </p></td> 
 </tr> 
</table>

Si `scl=` vient après `wid=` ou `hei=` dans l’URL, il annule ces commandes et `scl=` définit la taille de l’image renvoyée par le serveur.

Cependant, si `wid=` ou `hei=` vient après `scl=` dans l’URL, ils annulent `scl=` et `wid=`/ `hei=` définissent la taille de l’image renvoyée par le serveur.

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l’image de réponse calculée ou par défaut est supérieure à `attribute::MaxPix`.

## Propriétés {#section-170458cbd6984bd59a3434431258b20f}

Peut se produire n’importe où dans la requête. Ignoré si `wid=` ou `hei=` se produire après `scl=` dans la séquence de commandes.

Le redimensionnement de l’image avec `scl=` ne modifie pas la valeur de résolution d’impression incorporée dans l’image de réponse.

## Par défaut {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

Si `wid=`, `hei=`ou `scl=` ne sont pas spécifiées, l’image de réponse est mise à l’échelle pour correspondre à la taille définie par `attribute::DefaultPix`. Si `attribute::DefaultPix` est vide, l’image de réponse a la même taille que l’image de vue de la vignette.

## Voir aussi {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [attribute ::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [attribute ::D efaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
