---
title: effet
description: Sélectionnez Calque d’effet. Sélectionne un calque d’effet et lance un nouveau segment de calque dans la chaîne de requête qui est associée au calque actif.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# effet{#effect}

Sélectionnez Calque d’effet. Sélectionne un calque d’effet et lance un nouveau segment de calque dans la chaîne de requête qui est associée au calque actif.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Numéro du calque d'effet (int différent de 0). </p></td> 
 </tr> 
</table>

Toutes les commandes du nouveau segment sont appliquées au calque d’effet spécifié. Un segment de calque d’effet est terminé par la commande `layer=` ou `effect=` suivante ou par la fin de la requête.

La valeur *`n`* doit être inférieure à 0 pour les effets de calque externe (c&#39;est-à-dire les effets derrière le calque parent) et supérieure à 0 pour les effets de calque interne (c&#39;est-à-dire les effets au sein du calque parent). Il n&#39;est pas nécessaire que les numéros de calque d&#39;effet soient consécutifs.

Le numéro du calque d&#39;effet spécifie l&#39;ordre de plan, s&#39;il existe plusieurs calques d&#39;effet pour le même calque parent. Les calques dont la numérotation est supérieure sont placés au-dessus des calques dont la numérotation est inférieure.

Les calques d&#39;effet peuvent être attachés aux `layer=comp`.

## Propriétés {#section-e11f795deff345779ce280a82cf221ca}

Commande de calque d&#39;effet. La valeur *`n`* ne doit pas être 0.

## Par défaut {#section-84bbe1cfe7a94040827c994323ac59d4}

Aucune

## Exemple {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Voir aussi {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
