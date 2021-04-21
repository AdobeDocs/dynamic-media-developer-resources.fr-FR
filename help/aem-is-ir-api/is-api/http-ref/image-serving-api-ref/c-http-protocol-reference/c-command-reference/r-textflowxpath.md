---
description: Zone d’exclusion d’enchaînement de texte. Indique une ou plusieurs régions à exclure de l’enchaînement de texte.
solution: Experience Manager
title: textFlowXPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 8%

---


# textFlowXPath{#textflowxpath}

Zone d’exclusion d’enchaînement de texte. Indique une ou plusieurs régions à exclure de l’enchaînement de texte.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

Voir [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) pour plus d’informations, y compris une description de *`pathDefinition`*. Si aucune définition de chemin n&#39;est spécifiée, `textFlowXPath=` est ignoré.

## Propriétés {#section-cd1ebb151d4a405fbfc508d46522d686}

Attribut de calque de texte ( `textPs=` uniquement). Ignoré par d&#39;autres calques ou spécifié sans `textFlowPath=`. S&#39;applique à `layer=0` si spécifié pour `layer=comp`.

## Par défaut {#section-9405cda904684d829ed12a9e40a4dc46}

Aucune

## Voir aussi {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
