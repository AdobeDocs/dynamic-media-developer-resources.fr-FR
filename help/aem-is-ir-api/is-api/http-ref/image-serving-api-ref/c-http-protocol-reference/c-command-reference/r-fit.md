---
description: Mode d’ajustement de l’image de réponse. Indique le mode de calcul du facteur d’échelle, qui est utilisé pour mettre à l’échelle l’image composite avec l’image de réponse lorsque la taille de la réponse est spécifiée avec wid= et hei= et scl= n’est pas présente.
seo-description: Mode d’ajustement de l’image de réponse. Indique le mode de calcul du facteur d’échelle, qui est utilisé pour mettre à l’échelle l’image composite avec l’image de réponse lorsque la taille de la réponse est spécifiée avec wid= et hei= et scl= n’est pas présente.
seo-title: ajuster
solution: Experience Manager
title: ajuster
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 2%

---


# ajuster{#fit}

Mode d’ajustement de l’image de réponse. Indique le mode de calcul du facteur d’échelle, qui est utilisé pour mettre à l’échelle l’image composite avec l’image de réponse lorsque la taille de la réponse est spécifiée avec wid= et hei= et scl= n’est pas présente.

` fit= *``*, *`modeupscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mode  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|contrainte|recadrage|enveloppement|étirement|ajustement|ajustement  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> haut  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

Dans la description suivante des options de mode, on suppose que *`xScale`* est le rapport entre la largeur de l&#39;image composite et la largeur de l&#39;image de réponse et *`yScale`* le rapport entre la hauteur de l&#39;image composite et la hauteur de l&#39;image de réponse.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Paramètre </th> 
   <th colname="col2" class="entry"> Définition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> ajuster </span> </p> </td> 
   <td colname="col2"> <p>Met à l’échelle l’image composite afin qu’elle s’adapte à l’espace alloué avec <span class="codeph"> wid= </span> et <span class="codeph"> hei= </span>, avec un espace blanc minimal et sans recadrage. La taille exacte de l'image de réponse est spécifiée avec <span class="codeph"> wid= </span> et <span class="codeph"> hei= </span>. La plus petite de <span class="varname"> xScale </span> et <span class="varname"> yScale </span> est appliquée. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> contrainte  </span> </p> </td> 
   <td colname="col2"> <p>Met à l’échelle l’image composite comme <span class="codeph"> fit </span> de sorte qu’elle s’insère dans l’espace alloué avec <span class="codeph"> wid= </span> et <span class="codeph"> hei= </span>, mais l’image de réponse réelle peut être plus petite que celle spécifiée avec <span class="codeph"> wid= </span> hei= </span> pour éviter les espaces blancs. <span class="codeph"> La plus petite de <span class="varname"> xScale </span> et <span class="varname"> yScale </span> est appliquée. </span></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> Recadrer </span> </p> </td> 
   <td colname="col2"> <p>Met à l’échelle l’image composite de sorte qu’elle remplisse l’image de réponse complète, avec un recadrage minimal et sans espace blanc. La plus grande de <span class="varname"> xScale </span> et <span class="varname"> yScale </span> est appliquée. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> inclusion </span> </p> </td> 
   <td colname="col2"> <p>Met à l’échelle l’image composite telle que <span class="codeph"> recadrage </span> de sorte qu’elle couvre l’ensemble de l’image de réponse, mais l’image de réponse réelle peut être plus grande que celle spécifiée par <span class="codeph"> wid= </span> et <span class="codeph"> hei= </span> pour éviter le recadrage. La plus grande de <span class="varname"> xScale </span> et <span class="varname"> yScale </span>est appliquée. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> étirer  </span> </p> </td> 
   <td colname="col2"> <p>Met l’image composite à l’échelle de manière indépendante en x et y pour remplir l’image de réponse entière, sans recadrage ni espace blanc. Cela modifie généralement les proportions de l’image. <span class="varname"> xScale  </span> est utilisé pour la mise à l’échelle horizontale et  <span class="varname"> yScale  </span> pour la mise à l’échelle verticale. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> tenir  </span> </p> </td> 
   <td colname="col2"> <p>Applique <span class="varname"> xScale </span> à l'image de manière à l'ajuster horizontalement, avec un recadrage probable ou un espace blanc en haut et/ou en bas. Utile pour les applications spéciales. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> habiller  </span> </p> </td> 
   <td colname="col2"> <p>Applique <span class="varname"> yScale </span> à l'image de manière à l'ajuster verticalement, avec un recadrage probable ou un espace blanc à gauche et/ou à droite. Utile pour les applications spéciales. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définissez *`upscale`* sur &quot;1&quot; pour autoriser la mise à l’échelle ou sur &quot;0&quot; pour contraindre *`xScale`*et *`yScale`* à être limité à 1:1. Si la mise à l’échelle est désactivée, d’autres espaces blancs peuvent s’afficher si l’image composite est plus petite que l’image de réponse.

Les espaces de recadrage et les espaces sont centrés par défaut ; leur position peut être contrôlée avec `align=`. La couleur et l&#39;opacité du remplissage de l&#39;espace blanc sont déterminées par `bgc=`.

## Propriétés {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Attribut de vue. S’applique quel que soit le paramètre de calque actif. Au moins l&#39;un des `wid=` ou `hei=` doit également être spécifié, sinon une erreur est renvoyée. `wid=` et `hei=` doivent être spécifiés pour que les modes d&#39;ajustement se comportent comme décrit. Une erreur est renvoyée lorsque `req=tmb` est également spécifié.

## Par défaut {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Voir aussi {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
