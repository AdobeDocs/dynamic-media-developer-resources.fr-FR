---
description: Chemin d’accès de l’élément de calque inversé. Spécifie un chemin d’accès à l’élément d’exclusion pour le calque actif. Toutes les parties du calque situées dans la zone définie par clipXPath= sont rendues transparentes.
seo-description: Chemin d’accès de l’élément de calque inversé. Spécifie un chemin d’accès à l’élément d’exclusion pour le calque actif. Toutes les parties du calque situées dans la zone définie par clipXPath= sont rendues transparentes.
seo-title: clipXPath
solution: Experience Manager
title: clipXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a4062f3f-5dba-4514-acde-e1b7d608a2e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# clipXPath{#clipxpath}

Chemin d’accès de l’élément de calque inversé. Spécifie un chemin d’accès à l’élément d’exclusion pour le calque actif. Toutes les parties du calque situées dans la zone définie par clipXPath= sont rendues transparentes.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span></span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Nom du chemin d’accès incorporé dans l’image source du calque (ASCII uniquement). </p></td> 
 </tr> 
</table>

Voir [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) pour plus d’informations, y compris la description de ` *`pathName`*` et de ` *`pathDefinition`*`.

## Propriétés {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Attribut de calque. S’applique au calque actif ou à l’image composite, le cas échéant `layer=comp`. Ignoré si `clipPath=` n’est pas spécifié. Ignoré par les calques d’effet.

## Par défaut {#section-d1986aa31af14767aeb1b4a57add67f4}

Aucune

## Voir aussi {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
