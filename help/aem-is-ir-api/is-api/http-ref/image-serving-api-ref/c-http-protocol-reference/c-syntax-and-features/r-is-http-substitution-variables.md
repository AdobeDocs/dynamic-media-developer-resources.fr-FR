---
description: Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de demande vers des modèles de composition stockés dans les catalogues d’images. Les variables peuvent également être utilisées pour transmettre la même valeur à différents endroits dans une requête complexe.
solution: Experience Manager
title: Variables de substitution
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Variables de substitution{#substitution-variables}

Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de demande vers des modèles de composition stockés dans les catalogues d’images. Les variables peuvent également être utilisées pour transmettre la même valeur à différents endroits dans une requête complexe.

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom de la variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur à laquelle la variable doit être définie (chaîne). </p> </td> 
 </tr> 
</table>

Les définitions et références de variables peuvent apparaître dans la partie requête de la requête, dans `catalog::Modifier` et dans `catalog::PostModifier`.

Les variables sont définies comme ci-dessus, comme les autres commandes IS ; le &quot;$&quot; au début identifie la commande comme une définition de variable. Les variables doivent être définies avant d’être référencées.

Le nom de variable *`var`* n’est pas sensible à la casse et peut se composer de n’importe quelle combinaison de lettres ASCII, de nombres, de &quot;-&quot;, de &quot;_&quot; et de &quot;.&quot;.

>[!NOTE]
>
>*`value`* doit être codé URL à un seul passage pour une transmission HTTP sécurisée. Un double encodage est requis si *`value`* est retransmis via HTTP. C’est le cas lorsque *`value`* est remplacé dans une requête étrangère imbriquée ou dans l’attribut href d’un élément SVG `<image>`.

Les références de variable se composent du nom de variable délimité par le &quot;$&quot; de début et de fin ($*var*$). Les références peuvent se produire n’importe où dans la partie valeur de toute commande IS (c’est-à-dire entre le &quot;=&quot; suivant le nom de la commande et le &quot;&amp;&quot; suivant ou la fin de la requête). Les variables personnalisées ne peuvent pas être appliquées aux commandes `layer=` et `effect=`. Plusieurs variables sont autorisées dans la même valeur de commande. Le serveur remplace chaque occurrence de ` $ *`var`*$` par *`value`*.

Les références de variables peuvent ne pas être imbriquées. Les occurrences de ` $ *`var`*$` dans *`value`* ne sont pas remplacées.

Par exemple, le fragment de requête :

`$var2=apple&$var1=my$var2$tree&text=$var1$`

est résolu sur :

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; n’est pas un caractère réservé ; il peut se produire autrement dans la requête. Par exemple, `src=my$image$file.tif` est une commande valide (en supposant qu’il existe une entrée de catalogue ou un fichier image nommé `my$image$file.tif`), contrairement à `wid=$number$`, car `wid` nécessite un argument numérique.

## Traitement des variables dans les requêtes imbriquées {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *``*$` les références de variable peuvent se trouver n’importe où dans les accolades d’une demande de rendu d’image ou de diffusion d’image imbriquée, y compris à gauche de &quot;?&quot; séparant le chemin de la requête. Le serveur remplace ces références par des valeurs (provenant de l’URL ou de `catalog::Modifier` du catalogue d’images principal) avant d’analyser et de traiter davantage la requête imbriquée.

En outre, toutes les définitions ` $ *`var`*=` de l’URL ou `catalog::Modifier` sont transférées à toutes les demandes de diffusion d’images et de rendu d’images imbriquées. Cela garantit que toutes les définitions de variable sont disponibles pour tous les modèles, quel que soit le niveau d’imbrication.

Quel que soit le niveau d’imbrication, seul un codage HTTP à un seul passage doit être appliqué aux valeurs de variable qui doivent être remplacées n’importe où dans les demandes de rendu d’image ou de diffusion d’images imbriquées ou dans les chaînes `catalog::Modifier` associées.

## Traitement variable dans les requêtes étrangères incorporées {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`Les références de variable `*$`  se trouvant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes. Cela permet de placer des requêtes étrangères incorporées dans un modèle dans un catalogue d’images.

Les valeurs de variable qui doivent être remplacées par des requêtes étrangères doivent généralement être codées en double encodage, car aucun réencodage n’est appliqué avant que le serveur ne tente de transmettre l’URL étrangère finale.

## Traitement des variables dans les fichiers SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *``*$` les références de variables peuvent se produire dans les fichiers SVG dans les valeurs d’attribut et dans  `<text>` les chaînes. Le service d’images les remplace par les définitions ` $ *`var`*=` correspondantes connues au niveau d’imbrication de requête au niveau duquel le fichier SVG est spécifié.

>[!NOTE]
>
>Toute valeur de variable qui doit être remplacée par une valeur d’attribut `href` doit être codée en double URL ; tous les autres doivent être codés de manière unique.

## Variable de chemin prédéfinie {#section-930d0dd12e8f49499becc9fe8df24092}

La valeur *`object`* spécifiée dans le chemin de requête est affectée à la variable prédéfinie `*`$object`*`. &quot;` $ *`object`*$`&quot; peut être placé n’importe où dans la requête, dans le modèle référencé par la requête ou dans une requête imbriquée/incorporée où cet objet est autorisé, y compris la valeur de `src=` et `mask=`, et le chemin d’accès d’une requête imbriquée/incorporée.

Par exemple, la requête suivante réutilise l’image spécifiée dans le chemin en tant que source d’un calque dans une requête imbriquée :

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Cela équivaut à

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

La définition de `*`$object`*` peut être remplacée en spécifiant explicitement ` $ *`object`*=` avec la valeur souhaitée.

La variable de chemin prédéfinie est généralement utilisée conjointement avec `template=`.

## Par défaut {#section-b02483d15529444586a2e9504805b155}

Aucun. Seules les variables qui ont été définies seront remplacées par le serveur (à l’exception de la variable de chemin prédéfinie $object, qui sera toujours remplacée). Toutes les occurrences de ` $ *`var`*$` restent littérales si `*`var`*`ne peuvent pas être associées à une définition de variable existante.

## Exemples {#section-fba9393df6984247b7e30b3f93992e86}

Voir &quot;Exemple A&quot; dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
