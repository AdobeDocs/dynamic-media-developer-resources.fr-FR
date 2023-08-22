---
title: textFlowXPath
description: Zone d’exclusion de flux de texte. Spécifie une ou plusieurs régions à exclure du flux de texte.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 7%

---

# textFlowXPath{#textflowxpath}

Zone d’exclusion de flux de texte. Spécifie une ou plusieurs régions à exclure du flux de texte.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

Voir [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) pour plus d’informations, y compris une description de *`pathDefinition`*. Si aucune définition de chemin n’est spécifiée, `textFlowXPath=` est ignorée.

## Propriétés {#section-cd1ebb151d4a405fbfc508d46522d686}

Attribut de calque de texte ( `textPs=` uniquement). Ignoré par d’autres calques ou lorsqu’il est spécifié sans `textFlowPath=`. S’applique à `layer=0` si spécifié pour `layer=comp`.

## Par défaut {#section-9405cda904684d829ed12a9e40a4dc46}

Aucune

## Voir aussi {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
