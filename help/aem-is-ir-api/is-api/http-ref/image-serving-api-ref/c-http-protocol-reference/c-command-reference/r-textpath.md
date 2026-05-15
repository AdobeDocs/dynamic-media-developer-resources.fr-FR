---
title: textPath
description: Chemin du texte. Indique le chemin d’accès à utiliser comme ligne de base pour le texte fourni avec textPs=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
TQID: 'https://experienceleague.adobe.com/zVKtDOaScVXM-69CquAw4cpc81Wj7X47LLxBf0RdJ6c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 2%

---

# textPath{#textpath}

Chemin du texte. Indique le chemin d’accès à utiliser comme ligne de base pour le texte fourni avec textPs=.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Données de chemin. </p></td> 
 </tr> 
</table>

Voir [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) pour plus d’informations, y compris une description des *`pathDefinition`*.

>[!NOTE]
>
>Différent de `clipPath=`, les chemins de texte ne sont pas fermés automatiquement lorsque &#39;z&#39; ou &#39;Z&#39; n&#39;est pas spécifié à la fin d&#39;un sous-chemin.

*`pathDefinition`* peut inclure plusieurs sous-chemins d’accès. Le texte est rendu sur les sous-chemins dans l’ordre spécifié.

Les commandes RTF `\ql`, `\qc`, `\qr`, `\li` et `\ri` peuvent être utilisées pour positionner le texte rendu le long du chemin.

## Propriétés {#section-068137df436c46b9b55d271eb60e7285}

Attribut de calque de texte ( `textPs=` uniquement). Ignoré par les autres calques. S’applique à `layer=0` si spécifié pour `layer=comp`. Ignoré si `textPs=` sont présents.

Une erreur est renvoyée si un calque contient à la fois `textPath=` et `textFlowPath=`.

## Par défaut {#section-697b1f2cfc43498080a31327e6eb173d}

Aucune, pour le rendu de texte standard.

## Voir aussi {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [Calques de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
