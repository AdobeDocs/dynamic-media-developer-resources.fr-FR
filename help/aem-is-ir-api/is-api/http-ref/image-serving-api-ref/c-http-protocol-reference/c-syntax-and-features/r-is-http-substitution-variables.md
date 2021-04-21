---
description: Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de requête vers des modèles de composition stockés dans des catalogues d’images. Les variables peuvent également être utilisées pour transmettre la même valeur à différents emplacements dans une requête complexe.
solution: Experience Manager
title: Variables de substitution
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---


# Variables de substitution{#substitution-variables}

Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de requête vers des modèles de composition stockés dans des catalogues d’images. Les variables peuvent également être utilisées pour transmettre la même valeur à différents emplacements dans une requête complexe.

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom de variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur à laquelle la variable doit être définie (chaîne). </p> </td> 
 </tr> 
</table>

Les définitions de variable et les références peuvent se trouver dans la partie requête de la requête, dans `catalog::Modifier` et dans `catalog::PostModifier`.

Les variables sont définies comme ci-dessus, comme les autres commandes IS ; l&#39;en-tête &#39;$&#39; identifie la commande comme une définition de variable. Les variables doivent être définies avant d’être référencées.

Le nom de variable *`var`* n&#39;est pas sensible à la casse et peut se composer de n&#39;importe quelle combinaison de lettres ASCII, de chiffres, de &#39;-&#39;, de &#39;_&#39; et de &#39;.&#39;.

>[!NOTE]
>
>*`value`* doit être codé en URL à un seul passage pour une transmission HTTP sécurisée. Un codage par doublon est requis si *`value`* est retransmis via HTTP. C&#39;est le cas lorsque *`value`* est remplacé dans une requête étrangère imbriquée ou dans l&#39;attribut href d&#39;un élément SVG `<image>`.

Les références de variable se composent du nom de variable délimité par &#39;$&#39; de début et de fin ($*var*$). Les références peuvent se produire n&#39;importe où dans la partie valeur de toute commande IS (c&#39;est-à-dire entre le signe &quot;=&quot; suivant le nom de la commande et le caractère &quot;&amp;&quot; suivant ou la fin de la requête). Les variables personnalisées ne peuvent pas être appliquées aux commandes `layer=` et `effect=`. Plusieurs variables sont autorisées dans la même valeur de commande. Le serveur remplace chaque occurrence de ` $ *`var`*$` par *`value`*.

Les références de variable ne peuvent pas être imbriquées. Les occurrences de ` $ *`var`*$` dans *`value`* ne sont pas remplacées.

Par exemple, le fragment de requête :

`$var2=apple&$var1=my$var2$tree&text=$var1$`

est résolu à :

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; n&#39;est pas un caractère réservé ; il peut se produire autrement dans la demande. Par exemple, `src=my$image$file.tif` est une commande valide (en supposant qu’une entrée de catalogue ou un fichier image nommé `my$image$file.tif` existe), contrairement à `wid=$number$`, car `wid` nécessite un argument numérique.

## Traitement des variables dans les requêtes imbriquées {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`Les références de `*$` variable peuvent se trouver n’importe où dans les accolades d’une demande de diffusion d’images ou de rendu d’image imbriquée, y compris à gauche de l’&quot;?&quot; séparant le chemin de la requête. Le serveur remplace ces références par des valeurs (provenant de l’URL ou de `catalog::Modifier` du catalogue d’images principal) avant d’analyser et de traiter davantage la demande imbriquée.

En outre, toutes les définitions de ` $ *`var`*=` provenant de l’URL ou de `catalog::Modifier` sont transférées à toutes les demandes de diffusion d’images et de rendu d’image imbriquées. Ainsi, toutes les définitions de variable sont disponibles pour tous les modèles, quel que soit le niveau d’imbrication.

Quel que soit le niveau d’imbrication, seul le codage HTTP à une seule passe doit être appliqué aux valeurs de variable qui doivent être remplacées n’importe où dans les demandes de rendu d’image ou de diffusion d’image imbriquées ou dans les chaînes `catalog::Modifier` associées.

## Traitement variable des demandes étrangères incorporées {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`Les références de `*$` variable survenant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes. Cela permet de placer des requêtes étrangères incorporées dans un modèle dans un catalogue d’images.

En règle générale, les valeurs de variable devant être substituées dans des demandes étrangères doivent être codées en doublon, car aucun réencodage n’est appliqué avant que le serveur ne tente de transmettre l’URL étrangère finale.

## Traitement des variables dans les fichiers SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *`Les références `*$` de variable peuvent se produire dans les fichiers SVG dans les valeurs d’attribut et dans  `<text>` les chaînes. La fonction Image Serving les remplace par les définitions ` $ *`var`*=` correspondantes, connues au niveau d’imbrication de la demande au niveau duquel le fichier SVG est spécifié.

>[!NOTE]
>
>Toute valeur de variable qui doit être remplacée par une valeur d&#39;attribut `href` doit être encodée en URL de doublon ; tous les autres doivent être codés de manière unique.

## Variable de chemin prédéfinie {#section-930d0dd12e8f49499becc9fe8df24092}

L&#39;*`object`* spécifié dans le chemin de requête est affecté à la variable prédéfinie `*`$object`*`. &quot; ` $ *`object`*$`&quot; peut être placé n’importe où dans la requête, dans le modèle référencé par la requête ou dans une requête imbriquée/incorporée lorsque cet objet est autorisé, y compris la valeur `src=` et `mask=`, ainsi que le chemin d’une requête imbriquée/incorporée.

Par exemple, la requête suivante réutilise l’image spécifiée dans le chemin en tant que source d’un calque dans une requête imbriquée :

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Cela équivaut à

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

La définition de `*`$object`*` peut être remplacée en spécifiant explicitement ` $ *`object`*=` avec la valeur souhaitée.

La variable de chemin prédéfinie est généralement utilisée conjointement avec `template=`.

## Par défaut {#section-b02483d15529444586a2e9504805b155}

Aucun. Seules les variables définies seront remplacées par le serveur (à l’exception de la variable de chemin prédéfinie $object, qui sera toujours remplacée). Les occurrences de ` $ *`var`*$` restent littérales si `*`var`*`ne peuvent pas être associées à une définition de variable existante.

## Exemples {#section-fba9393df6984247b7e30b3f93992e86}

Voir &quot;Exemple A&quot; dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
