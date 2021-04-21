---
description: Zone de flux de texte. Spécifie une ou plusieurs régions dans lesquelles le texte spécifié avec textPs= doit être enchaîné.
solution: Experience Manager
title: textFlowPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---


# textFlowPath{#textflowpath}

Zone de flux de texte. Spécifie une ou plusieurs régions dans lesquelles le texte spécifié avec textPs= doit être enchaîné.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition  </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p> </td> 
 </tr> 
</table>

Voir [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) pour plus d’informations, y compris une description de *`pathDefinition`*.

Les commandes de marge RTF `\margl`, `\margr`, `\margt` et `\margb` sont ignorées lorsque `textFlowPath=` est présent. Si aucune définition de chemin n&#39;est spécifiée, `textFlowPath=` est ignoré.

## Propriétés {#section-b68dc887c6534ce8982cad740b3aeaa4}

Attribut de calque de texte ( `textPs=` uniquement). Ignoré par d’autres calques. S&#39;applique à `layer=0` si spécifié pour `layer=comp`.

## Par défaut {#section-68c4559b9e8242059b82e5a39a455dfc}

Identique au rectangle du calque ; le texte remplit l’intégralité du rectangle du calque.

## Voir aussi {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15), Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)[
