---
description: Texte du calque. Indique le texte et le formatage du contenu d’un calque de texte.
solution: Experience Manager
title: texte
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 5%

---


# texte{#text}

Texte du calque. Indique le texte et le formatage du contenu d’un calque de texte.

` text= *`chaîne`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chaîne </span> </p> </td> 
  <td class="stentry"> <p>Chaîne RTF (Rich-text-formatted) ou chaîne de texte brut. </p> </td> 
 </tr> 
</table>

Toutes les commandes de mise en forme des polices, des polices et des paragraphes sont exécutées à l’aide des commandes RTF. Pour plus d’informations, voir [Formatage de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`text=` prend en charge la mise à l’échelle automatique du texte pour remplir le rectangle de calque spécifié par  `size=`.

Voir [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` prend en charge le dimensionnement automatique du calque de texte pour l’adapter au texte rendu (lorsque ce n’ `size=` est pas spécifié ou lorsque seule la largeur est spécifiée). Notez que, dans ce cas, seule l&#39;une des commandes d&#39;alignement RTF `\ql`, `\qr` et `\qc` peut être appliquée ; sinon, une erreur est renvoyée.

## Propriétés {#section-8c0f020094a44c6b858454ef91ab4edf}

Attribut de couche. S&#39;applique à `layer=0` si `layer=comp`. Mutuellement exclusif avec `src=` et `textPs=` dans la même couche ; la dernière occurrence de `text=`, `textPs=` et `src=` prévaut et détermine s’il s’agit d’une image ou d’un calque de texte. Ignoré par les calques d’effet.

## Par défaut {#section-58958671e0ad479e8d5f6c1d41d7dc74}

Aucune

## Exemple {#section-d011f765ec5c418d814a821019b0eef0}

Voir les exemples de [Formatage de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) et [Exemple A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-207b779ab67342a5acd343e6bcc749c4}

[Formatage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) du texte, Positionnement [ du ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87)texte,  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)[
