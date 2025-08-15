---
title: adapter
description: Mode d’ajustement de l’image de réponse. Indique comment le facteur d’échelle est calculé, qui est utilisé pour mettre à l’échelle l’image composite par rapport à l’image de réponse lorsque la taille de réponse est spécifiée avec les valeurs wid= et hei= et scl= n’est pas présente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 1%

---

# adapter{#fit}

Mode d’ajustement de l’image de réponse. Indique comment le facteur d’échelle est calculé, qui est utilisé pour mettre à l’échelle l’image composite par rapport à l’image de réponse lorsque la taille de réponse est spécifiée avec les valeurs wid= et hei= et scl= n’est pas présente.

` fit= *`mode`*, *`upscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mode </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ajuster|contraindre|recadrer|enrouler|étirer|ajuster|ajuster</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> </span> </span> haut de gamme </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

Dans la description suivante des options de mode, on suppose que *`xScale`* est le rapport de la largeur de l’image composite sur la largeur de l’image de réponse et *`yScale`* est le rapport de la hauteur de l’image composite sur la hauteur de l’image de réponse.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Paramètre </th> 
   <th colname="col2" class="entry"> Définition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> adaptée </span> </p> </td> 
   <td colname="col2"> <p>Met à l’échelle l’image composite afin qu’elle s’adapte à l’espace alloué avec <span class="codeph"> wid= </span> et <span class="codeph"> hei= </span>, avec un espace blanc minimal et aucun recadrage. L’image de réponse a la taille exacte spécifiée avec <span class="codeph"> wid= </span> et <span class="codeph"> hei= </span>. La plus petite des valeurs suivantes est appliquée : <span class="varname"> xScale </span> et <span class="varname"> yScale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> de contrainte </span> </p> </td> 
   <td colname="col2"> <p>Met à l’échelle l’image composite de la même manière que <span class="codeph"> adapte </span> afin qu’elle s’adapte à l’espace alloué avec <span class="codeph"> wid= </span> et <span class="codeph"> hei= </span>, mais l’image de réponse réelle peut être plus petite que celle spécifiée avec <span class="codeph"> wid= </span> et <span class="codeph"> hei= </span> pour éviter les espaces. La plus petite des valeurs suivantes est appliquée : <span class="varname"> xScale </span> et <span class="varname"> yScale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> de recadrage </span> </p> </td> 
   <td colname="col2"> <p>Met à l’échelle l’image composite de sorte qu’elle remplisse l’ensemble de l’image de réponse, avec un recadrage minimal et aucun espace blanc. La plus grande des valeurs <span class="varname"> xScale </span> et <span class="varname"> yScale </span> est appliquée. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> wrap </span> </p> </td> 
   <td colname="col2"> <p>Met à l’échelle l’image composite comme <span class="codeph"> </span>’image de recadrage de sorte qu’elle couvre l’ensemble de l’image de réponse, mais l’image de réponse réelle peut être plus grande que celle spécifiée avec <span class="codeph"> wid= </span> et <span class="codeph"> hei= </span> pour éviter le recadrage. La plus grande des valeurs <span class="varname"> xScale </span> et <span class="varname"> yScale </span>est appliquée. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> d’étirement </span> </p> </td> 
   <td colname="col2"> <p>Met à l’échelle l’image composite indépendamment dans x et y pour remplir l’image de réponse entière, sans recadrage ni espace blanc. Cela modifie généralement les proportions de l’image. <span class="varname"> xScale </span> est utilisé pour la mise à l’échelle horizontale et <span class="varname"> yScale </span> pour la mise à l’échelle verticale. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>Applique <span class="varname"> xScale </span> pour ajuster étroitement l’image horizontalement, avec un recadrage ou un espace en haut et/ou en bas. Utile pour les applications spéciales. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>Applique <span class="varname">’</span> yScale pour ajuster étroitement l’image verticalement, avec un recadrage ou un espace probable à gauche et/ou à droite. Utile pour les applications spéciales. </p> </td> 
  </tr> 
 </tbody> 
</table>

Définissez *`upscale`* sur « 1 » pour permettre la mise à l’échelle ou sur « 0 » pour limiter *`xScale`* et *`yScale`* être limité à 1:1. Si la mise à l’échelle est désactivée, des espaces supplémentaires peuvent être présents si l’image composite est plus petite que l’image de réponse.

Le recadrage et les espaces sont centrés par défaut ; leur position peut être contrôlée à l’aide de `align=`. La couleur et l’opacité du remplissage des espaces blancs sont déterminées par `bgc=`.

## Propriétés {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Attribut d’affichage. S’applique quel que soit le paramètre de calque actif. Au moins l’un des modes `wid=` ou `hei=` doit également être spécifié, sinon une erreur est renvoyée ; `wid=` et `hei=` doivent tous deux être spécifiés pour que les modes d’ajustement se comportent comme décrit. Une erreur est également renvoyée lorsque `req=tmb` est spécifié.

## Par défaut {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Voir aussi {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
