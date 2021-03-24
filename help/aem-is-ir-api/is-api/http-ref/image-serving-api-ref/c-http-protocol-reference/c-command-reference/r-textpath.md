---
description: Chemin d’accès au texte. Spécifie le chemin d’accès à utiliser comme ligne de base pour le texte fourni avec textPs=.
solution: Experience Manager
title: textPath
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---


# textPath{#textpath}

Chemin d’accès au texte. Spécifie le chemin d’accès à utiliser comme ligne de base pour le texte fourni avec textPs=.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

Voir [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) pour plus d’informations, y compris une description de *`pathDefinition`*.

>[!NOTE]
>
>Contrairement à `clipPath=`, les chemins de texte ne sont pas fermés automatiquement lorsque &#39;z&#39; ou &#39;Z&#39; n&#39;est pas spécifié à la fin d&#39;un sous-chemin.

*`pathDefinition`* peuvent inclure plusieurs sous-chemins. Le texte est rendu sur les sous-chemins dans l’ordre spécifié.

Les commandes RTF `\ql`, `\qc`, `\qr`, `\li` et `\ri` peuvent être utilisées pour positionner le texte rendu le long du chemin.

## Propriétés {#section-068137df436c46b9b55d271eb60e7285}

Attribut de calque de texte ( `textPs=` uniquement). Ignoré par d’autres calques. S&#39;applique à `layer=0` si spécifié pour `layer=comp`. Ignoré si `textPs=` est présent.

Une erreur est renvoyée si un calque contient à la fois `textPath=` et `textFlowPath=`.

## Par défaut {#section-697b1f2cfc43498080a31327e6eb173d}

Aucun, pour le rendu de texte standard.

## Voir aussi {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), calques de  [texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
