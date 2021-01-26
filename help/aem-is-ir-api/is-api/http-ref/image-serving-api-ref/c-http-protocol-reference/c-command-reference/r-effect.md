---
description: Sélectionnez Calque d’effets. Sélectionne un calque d’effets et début un nouveau segment de calque dans la chaîne de requête, qui est associé au calque actif.
seo-description: Sélectionnez Calque d’effets. Sélectionne un calque d’effets et début un nouveau segment de calque dans la chaîne de requête, qui est associé au calque actif.
seo-title: effet
solution: Experience Manager
title: effet
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 622dc7ca-55b8-4a82-b9a7-65588aee87d0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 3%

---


# effet{#effect}

Sélectionnez Calque d’effets. Sélectionne un calque d’effets et début un nouveau segment de calque dans la chaîne de requête, qui est associé au calque actif.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Numéro du calque d’effet (int différent de 0). </p></td> 
 </tr> 
</table>

Toutes les commandes du nouveau segment sont appliquées au calque d’effet spécifié. Un segment de couche d’effet est terminé par la commande suivante `layer=` ou `effect=` ou par la fin de la requête.

*`n`* doit être inférieur à 0 pour les effets de calque externe (c’est-à-dire les effets derrière le calque parent) et supérieur à 0 pour les effets de calque interne (c’est-à-dire les effets dans le calque parent). Les numéros des calques d’effets ne doivent pas nécessairement être consécutifs.

Le numéro de calque d’effet spécifie l’ordre z, en cas de plusieurs calques d’effets pour le même calque parent. Les calques à numérotation supérieure sont placés au-dessus des calques à numérotation inférieure.

Les couches d&#39;effets peuvent être associées à `layer=comp`.

## Propriétés {#section-e11f795deff345779ce280a82cf221ca}

Calque d’effet, commande. *`n`* ne doit pas être égal à 0.

## Par défaut {#section-84bbe1cfe7a94040827c994323ac59d4}

Aucune

## Exemple {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Voir aussi {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`
