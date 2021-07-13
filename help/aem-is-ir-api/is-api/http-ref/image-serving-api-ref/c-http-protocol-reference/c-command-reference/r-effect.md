---
description: Sélectionnez Calque d’effet. Sélectionne un calque d’effet et lance un nouveau segment de calque dans la chaîne de requête, qui est associé au calque actif.
solution: Experience Manager
title: effet
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---

# effet{#effect}

Sélectionnez Calque d’effet. Sélectionne un calque d’effet et lance un nouveau segment de calque dans la chaîne de requête, qui est associé au calque actif.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Numéro de calque de l’effet (int différent de 0). </p></td> 
 </tr> 
</table>

Toutes les commandes du nouveau segment sont appliquées à la couche d’effet spécifiée. Un segment de calque d’effet est arrêté par la commande `layer=` ou `effect=` suivante ou à la fin de la requête.

*`n`* doit être inférieur à 0 pour les effets de couche externe (c’est-à-dire les effets derrière la couche parent) et supérieur à 0 pour les effets de couche interne (c’est-à-dire les effets dans la couche parent). Les numéros de calque d’effet ne doivent pas nécessairement être consécutifs.

Le numéro de calque d’effet spécifie l’ordre z, dans le cas de plusieurs calques d’effet pour le même calque parent. Les calques à numéro supérieur sont placés au-dessus des calques à numéro inférieur.

Les calques d’effet peuvent être joints à `layer=comp`.

## Propriétés {#section-e11f795deff345779ce280a82cf221ca}

Couche d’effet, commande. *`n`* ne doit pas être égal à 0.

## Par défaut {#section-84bbe1cfe7a94040827c994323ac59d4}

Aucune

## Exemple {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Voir aussi {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`
