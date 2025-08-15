---
description: Les variables de substitution sont utilisées pour transférer les valeurs de l’URL de requête vers les modèles de composition stockés dans les catalogues d’images. Les variables peuvent également être utilisées pour transmettre la même valeur à différents endroits dans une requête complexe.
solution: Experience Manager
title: Variables de substitution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# Variables de substitution{#substitution-variables}

Les variables de substitution sont utilisées pour transférer les valeurs de l’URL de requête vers les modèles de composition stockés dans les catalogues d’images. Les variables peuvent également être utilisées pour transmettre la même valeur à différents endroits dans une requête complexe.

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom de la variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> valeur <span class="varname"> </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur à laquelle la variable doit être définie (chaîne). </p> </td> 
 </tr> 
</table>

Les définitions et références de variables peuvent se produire dans la partie requête de la requête, dans `catalog::Modifier` et dans `catalog::PostModifier`.

Les variables sont définies comme ci-dessus, de la même manière que les autres commandes IS ; le caractère &#39;$&#39; initial identifie la commande comme une définition de variable. Les variables doivent être définies avant d’être référencées.

Le nom de variable *`var`* n’est pas sensible à la casse et peut consister en une combinaison de lettres ASCII, de chiffres, de caractères « - », « _ » et « . ».

>[!NOTE]
>
>*`value`* doit être codé URL en une seule passe pour une transmission HTTP sécurisée. Un double encodage est requis si *`value`* est retransmis par le biais du protocole HTTP. C’est le cas lorsque la *`value`* est remplacée dans une requête étrangère imbriquée ou dans l’attribut href d’un élément de `<image>` SVG.

Les références de variable se composent du nom de variable délimité par les caractères de début et de fin « $ » ($*var*$). Les références peuvent apparaître n’importe où dans la partie valeur de n’importe quelle commande IS (c’est-à-dire entre le signe « = » suivant le nom de la commande et le signe «&amp; » suivant ou la fin de la requête). Les variables personnalisées ne peuvent pas être appliquées aux commandes `layer=` et `effect=`. Plusieurs variables sont autorisées dans la même valeur de commande. Le serveur remplace chaque occurrence de ` $ *`var`*$` par *`value`*.

Les références de variables ne peuvent pas être imbriquées. Les occurrences de ` $ *`var`*$` dans *`value`* ne sont pas remplacées.

Par exemple, le fragment de requête :

`$var2=apple&$var1=my$var2$tree&text=$var1$`

est résolu sur :

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; n’est pas un caractère réservé ; il peut se produire autrement dans la requête. Par exemple, `src=my$image$file.tif` est une commande valide (en supposant qu’une entrée de catalogue ou un fichier image nommé `my$image$file.tif` existe), tandis que `wid=$number$` ne l’est pas, car `wid` nécessite un argument numérique.

## Traitement des variables dans les requêtes imbriquées {#section-26d63adc446c4fa0808e11e8082abdfa}

Les références ` $ *`var`*$` peuvent se produire n’importe où dans les accolades d’une requête de diffusion d’images ou de rendu d’image imbriquée, y compris à gauche de « ? » en séparant le chemin d’accès de la requête. Le serveur remplace ces références par des valeurs (provenant de l’URL ou de l’`catalog::Modifier` du catalogue d’images principal) avant d’analyser et de traiter plus en détail la requête imbriquée.

En outre, toutes les définitions ` $ *`var`*=` de l’URL ou du `catalog::Modifier` sont transférées à toutes les requêtes de diffusion d’images et de rendu d’images imbriquées. Cela permet de s’assurer que toutes les définitions de variable sont disponibles pour tous les modèles, quel que soit le niveau d’imbrication.

Quel que soit le niveau d’imbrication, seul le codage HTTP à une seule passe doit être appliqué aux valeurs de variable qui doivent être remplacées n’importe où dans les requêtes de rendu d’image imbriquées ou de diffusion d’image ou leurs chaînes de `catalog::Modifier` associées.

## Traitement des variables dans des requêtes étrangères incorporées {#section-314e39a9aefb46faa737fd137897d1b0}

Les références ` $ *`var`*$` apparaissant n’importe où dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes. Cela permet de placer les requêtes étrangères incorporées dans un modèle de catalogue d’images.

Les valeurs de variable qui doivent être remplacées dans des requêtes étrangères doivent généralement être codées deux fois, car aucun recodage n’est appliqué avant que le serveur ne tente de transmettre l’url étrangère finale.

## Traitement des variables dans les fichiers SVG {#section-a8359f9909764142b6a18ae778dca913}

Les références ` $ *`var`*$` peuvent se produire dans les fichiers SVG dans les valeurs d’attribut et dans les chaînes de `<text>`. La diffusion d’images les remplace par les définitions ` $ *`var`*=` correspondantes connues au niveau d’imbrication de la requête auquel le fichier SVG est spécifié.

>[!NOTE]
>
>Toute valeur de variable à remplacer par une valeur d’attribut `href` doit être codée en double URL ; toutes les autres doivent être codées individuellement.

## Variable de chemin prédéfinie {#section-930d0dd12e8f49499becc9fe8df24092}

Le *`object`* spécifié dans le chemin d’accès de la requête est affecté à la variable prédéfinie `*`$object`*`. « ` $ *`object`*$` » peut être placé n’importe où dans la requête, dans le modèle référencé par la requête ou dans une requête imbriquée/incorporée où cet objet est autorisé, y compris la valeur de `src=` et `mask=`, ainsi que le chemin d’accès d’une requête imbriquée/incorporée.

Par exemple, la requête suivante réutilise l’image spécifiée dans le chemin d’accès en tant que source d’un calque dans une requête imbriquée :

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Cela équivaut à

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

La définition de `*`$object`*` peut être remplacée en spécifiant explicitement ` $ *`object`*=` avec la valeur souhaitée.

La variable de chemin prédéfinie est généralement utilisée conjointement avec `template=`.

## Par défaut {#section-b02483d15529444586a2e9504805b155}

Aucune. Seules les variables qui ont été définies sont remplacées par le serveur (à l’exception de la variable de chemin prédéfinie $object, qui est toujours remplacée). Les occurrences de ` $ *`var`*$` restent littérales si `*`var`*`ne peut pas être mise en correspondance avec une définition de variable existante.

## Exemples {#section-fba9393df6984247b7e30b3f93992e86}

Voir « Exemple A » dans [ Modèles ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
