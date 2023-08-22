---
title: texte
description: Texte du calque. Indique le texte et le contenu de mise en forme d’un calque de texte.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 5%

---

# texte{#text}

Texte du calque. Indique le texte et le contenu de mise en forme d’un calque de texte.

` text= *`chaîne`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chaîne </span> </p> </td> 
  <td class="stentry"> <p>Chaîne au format texte enrichi (RTF) ou chaîne en texte brut. </p> </td> 
 </tr> 
</table>

Toutes les commandes de police, de couleur de police et de mise en forme de paragraphe sont effectuées à l’aide des commandes RTF. Voir [Formatage de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) pour plus d’informations.

`text=` prend en charge la mise à l’échelle automatique du texte pour remplir le rectangle de calque spécifié par `size=`.

Voir [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` prend en charge le dimensionnement automatique du calque de texte pour l’adapter au texte rendu (lorsque `size=` n’est pas spécifié ou lorsque seule la largeur est spécifiée). Notez que, dans ce cas, seule une des commandes d&#39;alignement RTF `\ql`, `\qr`, et `\qc` peut être appliquée ; dans le cas contraire, une erreur est renvoyée.

## Propriétés {#section-8c0f020094a44c6b858454ef91ab4edf}

Attribut de calque. S’applique à `layer=0` if `layer=comp`. Mutuellement exclusif avec `src=` et `textPs=` dans le même calque ; la dernière occurrence de `text=`, `textPs=`, et `src=` prévaut et détermine s’il s’agit d’une image ou d’un calque de texte. Ignoré par les calques d’effet.

## Par défaut {#section-58958671e0ad479e8d5f6c1d41d7dc74}

Aucune

## Exemple {#section-d011f765ec5c418d814a821019b0eef0}

Voir les exemples de la section [Formatage de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) et [Exemple A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-207b779ab67342a5acd343e6bcc749c4}

[Formatage de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Positionnement de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
