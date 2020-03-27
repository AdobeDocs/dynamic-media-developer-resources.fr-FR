---
description: Les variables de substitution permettent de transférer des valeurs de l’URL de requête vers des modèles de composition stockés dans des catalogues d’images. Les variables peuvent également être utilisées pour transmettre la même valeur à différents emplacements dans une requête complexe.
seo-description: Les variables de substitution permettent de transférer des valeurs de l’URL de requête vers des modèles de composition stockés dans des catalogues d’images. Les variables peuvent également être utilisées pour transmettre la même valeur à différents emplacements dans une requête complexe.
seo-title: Variables de substitution
solution: Experience Manager
title: Variables de substitution
topic: Scene7 Image Serving - Image Rendering API
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Variables de substitution{#substitution-variables}

Les variables de substitution permettent de transférer des valeurs de l’URL de requête vers des modèles de composition stockés dans des catalogues d’images. Les variables peuvent également être utilisées pour transmettre la même valeur à différents emplacements dans une requête complexe.

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span></span> </p> </td> 
  <td class="stentry"> <p>Nom de variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valeur </span></span> </p> </td> 
  <td class="stentry"> <p>Valeur à laquelle la variable doit être définie (chaîne). </p> </td> 
 </tr> 
</table>

Les définitions de variable et les références peuvent se produire dans la partie  de la requête, dans `catalog::Modifier`et dans `catalog::PostModifier`.

Les variables sont définies comme ci-dessus, comme les autres commandes IS ; le caractère &quot;$&quot; en tête identifie la commande comme une définition de variable. Les variables doivent être définies avant d’être référencées.

Le nom de variable *`var`* n’est pas sensible à la casse et peut être composé de n’importe quelle combinaison de lettres ASCII, de nombres, de &quot;-&quot;, de &quot;_&quot; et de &quot;.&quot;.

>[!NOTE]
>
>*`value`* doit être codé en URL à un seul passage pour une transmission HTTP sécurisée. Le -codage est requis si *`value`* est retransmis via HTTP. C’est le cas lorsqu’ *`value`* il est remplacé dans une requête étrangère imbriquée ou dans l’attribut href d’un `<image>` élément SVG.

Les références de variable se composent du nom de la variable délimité par &#39;$&#39; en début et en fin ($*var*$). Les références peuvent se produire n’importe où dans la partie valeur de toute commande IS (c’est-à-dire entre le signe &quot;=&quot; qui suit le nom de la commande et le caractère &quot;&amp;&quot; suivant ou la fin de la requête). Les variables personnalisées ne peuvent pas être appliquées aux commandes `layer=` et `effect=` . Plusieurs variables sont autorisées dans la même valeur de commande. Le serveur remplace chaque occurrence de ` $ *`var`*$` par *`value`*.

Il est possible que les références aux variables ne soient pas imbriquées. Les occurrences de ` $ *`var`*$` dans *`value`* l’élément ne sont pas remplacées.

Par exemple, le fragment de requête :

`$var2=apple&$var1=my$var2$tree&text=$var1$`

est résolu à :

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; n&#39;est pas un caractère réservé ; il peut se produire autrement dans la requête. Par exemple, `src=my$image$file.tif` est une commande valide (en supposant qu’une entrée de catalogue ou un fichier image nommé `my$image$file.tif` existe), mais `wid=$number$` ne l’est pas, car `wid` requiert un argument numérique.

## Traitement des variables dans les requêtes imbriquées {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`Les références var`*$` peuvent se trouver n’importe où dans les accolades d’une demande imbriquée de diffusion d’images ou de rendu d’images, y compris à gauche du signe &quot;?&quot; séparant le chemin du . Le serveur remplace ces références par des valeurs (provenant de l’URL ou `catalog::Modifier` du catalogue d’images principal) avant d’analyser et de traiter davantage la requête imbriquée.

En outre, toutes les définitions de ` $ *`variables`*=` issues de l’URL ou `catalog::Modifier` sont transférées à toutes les demandes imbriquées de diffusion d’images et de rendu d’image. Ainsi, toutes les définitions de variable sont disponibles pour tous les modèles, quel que soit le niveau d’imbrication.

Quel que soit le niveau d’imbrication, seul un encodage HTTP unique doit être appliqué aux valeurs de variable qui doivent être remplacées n’importe où dans les demandes de rendu d’image ou de diffusion d’images imbriquées ou dans les `catalog::Modifier` chaînes associées.

## Traitement variable dans les requêtes étrangères incorporées {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`Les références de variable`*$` survenant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes. Cela permet de placer des requêtes étrangères incorporées dans un modèle dans un catalogue d’images.

En règle générale, les valeurs de variable devant être remplacées dans des requêtes étrangères doivent être codées en , car aucun réencodage n’est appliqué avant que le serveur ne tente de transmettre l’URL étrangère finale.

## Traitement des variables dans les fichiers SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *`Les références aux variables`*$` peuvent se produire dans les fichiers SVG dans les valeurs d’attribut et `<text>` les chaînes. Le serveur d’images les remplace par les définitions de ` $ *`var`*=` correspondantes connues au niveau d’imbrication de la requête au niveau duquel le fichier SVG est spécifié.

>[!NOTE]
>
>Toute valeur de variable qui doit être remplacée par une valeur d&#39; `href` attribut doit être encodée  URL ; tous les autres doivent être codés individuellement.

## Variable de chemin prédéfinie {#section-930d0dd12e8f49499becc9fe8df24092}

Le chemin *`object`* spécifié dans le chemin de requête est affecté à la variable prédéfinie ` *`$object`*`. &#39; ` $ *`object`*$`&#39; peut être placé n’importe où dans la requête, dans le modèle référencé par la requête, ou dans une requête imbriquée/incorporée lorsque cet objet est autorisé, y compris la valeur de `src=` et `mask=`, et le chemin d’une requête imbriquée/incorporée.

Par exemple, la requête suivante réutilise l’image spécifiée dans le chemin d’accès en tant que source d’un calque dans une requête imbriquée :

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Cela équivaut à

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

La définition de ` *`$object`*` peut être remplacée en spécifiant explicitement ` $ *`objet`*=` avec la valeur souhaitée.

La variable de chemin prédéfinie est généralement utilisée conjointement avec `template=`.

## Par défaut {#section-b02483d15529444586a2e9504805b155}

Aucun. Seules les variables définies seront remplacées par le serveur (à l’exception de la variable de chemin prédéfinie $object, qui sera toujours remplacée). Les occurrences de ` $ *`var`*$` restent littérales si ` *``*`varv ne peut pas être mise en correspondance avec une définition de variable existante.

## Exemples {#section-fba9393df6984247b7e30b3f93992e86}

Voir &quot;Exemple A&quot; dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
