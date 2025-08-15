---
title: clipXPath
description: Inversion du chemin Clip calque. Spécifie un chemin d’exclusion pour le calque actuel. Toutes les parties du calque qui se trouvent dans la zone définie par clipXPath= sont rendues transparentes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# clipXPath{#clipxpath}

Inversion du chemin Clip calque. Spécifie un chemin d’exclusion pour le calque actuel. Toutes les parties du calque qui se trouvent dans la zone définie par clipXPath= sont rendues transparentes.

`clipXPath= *`Définition du chemin`*`

`clipXPathE= *`Nom du chemin`*&#42;[, *`Nom du chemin`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Définition du</span> chemin </span> </p> </td> 
  <td class="stentry"> <p>Données de chemin. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Chemin</span> </span> </p> </td> 
  <td class="stentry"> <p>Nom du chemin incorporé dans l’image source du calque (ASCII uniquement). </p></td> 
 </tr> 
</table>

Voir [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) pour plus d’informations, y compris une description de pathName`*` et `*`pathDefinition`*``*`.

## Propriétés {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Attribut de calque. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré si `clipPath=` n’est pas spécifié. Ignoré par les calques d’effets.

## Par défaut {#section-d1986aa31af14767aeb1b4a57add67f4}

Aucune

## Voir aussi {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
