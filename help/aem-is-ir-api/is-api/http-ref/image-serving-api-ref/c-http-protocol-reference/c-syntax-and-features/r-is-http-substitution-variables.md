---
description: Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de demande vers des modèles de composition stockés dans les catalogues d’images. Les variables peuvent également être utilisées pour transmettre la même valeur à différents endroits dans une requête complexe.
solution: Experience Manager
title: Variables de substitution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Variables de substitution{#substitution-variables}

Les variables de substitution sont utilisées pour transférer des valeurs de l’URL de demande vers des modèles de composition stockés dans les catalogues d’images. Les variables peuvent également être utilisées pour transmettre la même valeur à différents endroits dans une requête complexe.

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom de la variable. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur à laquelle la variable doit être définie (chaîne). </p> </td> 
 </tr> 
</table>

Les définitions et références de variables peuvent se produire dans la partie requête de la requête, dans `catalog::Modifier`et dans `catalog::PostModifier`.

Les variables sont définies comme ci-dessus, comme les autres commandes IS ; le &quot;$&quot; au début identifie la commande comme une définition de variable. Les variables doivent être définies avant d’être référencées.

Nom de variable *`var`* n’est pas sensible à la casse et peut se composer de n’importe quelle combinaison de lettres ASCII, nombres, &quot;-&quot;, &quot;_&quot; et &quot;.&quot;.

>[!NOTE]
>
>*`value`* doit être codé URL à un seul passage pour une transmission HTTP sécurisée. Un double encodage est requis si *`value`* est retransmis par HTTP. C’est le cas lorsque *`value`* est remplacé dans une requête étrangère imbriquée ou dans l’attribut href d’un SVG `<image>` élément .

Les références de variable se composent du nom de variable délimité par le &quot;$&quot; de début et de fin ($)*var*$). Les références peuvent se produire n’importe où dans la partie valeur de toute commande IS (c’est-à-dire, entre le &quot;=&quot; suivant le nom de la commande et le &quot;&amp;&quot; suivant ou la fin de la requête). Les variables personnalisées ne peuvent pas être appliquées à la variable `layer=` et `effect=` des commandes. Plusieurs variables sont autorisées dans la même valeur de commande. Le serveur remplace chaque occurrence de ` $ *`var`*$` avec *`value`*.

Les références de variables peuvent ne pas être imbriquées. Toutes les occurrences de ` $ *`var`*$` dans *`value`* ne sont pas substituées.

Par exemple, le fragment de requête :

`$var2=apple&$var1=my$var2$tree&text=$var1$`

est résolu sur :

`text=my$var2$tree`

>[!NOTE]
>
>&quot;$&quot; n’est pas un caractère réservé ; il peut se produire dans la requête. Par exemple : `src=my$image$file.tif` est une commande valide (en supposant qu’une entrée de catalogue ou un fichier image nommé `my$image$file.tif` existe), alors que `wid=$number$` n’est pas , car `wid` nécessite un argument numérique.

## Traitement des variables dans les requêtes imbriquées {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` les références peuvent se trouver n’importe où dans les accolades d’une demande de rendu d’image ou de diffusion d’image imbriquée, y compris à gauche de l’icône ? séparant le chemin de la requête. Le serveur remplace ces références par des valeurs (provenant de l’URL ou de `catalog::Modifier` du catalogue d’images principal) avant d’analyser et de traiter plus en détail la requête imbriquée.

En outre, tous les ` $ *`var`*=` définitions de l’URL ou `catalog::Modifier` sont transférées à toutes les requêtes Image Serving et Image Rendering imbriquées. Cela garantit que toutes les définitions de variable sont disponibles pour tous les modèles, quel que soit le niveau d’imbrication.

Quel que soit le niveau d’imbrication, seul un codage HTTP à un seul passage doit être appliqué aux valeurs de variable qui doivent être remplacées n’importe où dans les demandes de rendu d’image ou de diffusion d’image imbriquées ou dans les demandes associées. `catalog::Modifier` chaînes.

## Traitement de variables dans des requêtes étrangères incorporées {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` les références se trouvant à un emplacement dans les accolades d’une requête étrangère incorporée sont remplacées par des valeurs de définition de variable correspondantes. Cela permet de placer des requêtes étrangères incorporées dans un modèle dans un catalogue d’images.

Les valeurs de variable qui doivent être remplacées par des requêtes étrangères doivent généralement être codées en double encodage, car aucun réencodage n’est appliqué avant que le serveur ne tente de transmettre l’URL étrangère finale.

## Traitement des variables dans les fichiers SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` les références peuvent se produire dans les fichiers de SVG dans les valeurs d’attribut et dans `<text>` chaînes. La diffusion d’images les remplace par la correspondance ` $ *`var`*=` définitions connues au niveau d’imbrication de requête auquel le fichier de SVG est spécifié.

>[!NOTE]
>
>Toute valeur de variable qui doit être remplacée par une `href` La valeur d’attribut doit être codée en double URL ; tous les autres doivent être codés en une seule fois.

## Variable de chemin prédéfinie {#section-930d0dd12e8f49499becc9fe8df24092}

La variable *`object`* spécifié dans le chemin de requête est affecté à la variable prédéfinie `*`$object`*`. &#39; ` $ *`objet`*$`&quot; peut être placé n’importe où dans la requête, dans le modèle référencé par la requête ou dans une requête imbriquée/incorporée lorsque cet objet est autorisé, y compris la valeur de `src=` et `mask=`et le chemin d’accès d’une requête imbriquée/incorporée.

Par exemple, la requête suivante réutilise l’image spécifiée dans le chemin comme source d’un calque dans une requête imbriquée :

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Cela équivaut à

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

La définition de `*`$object`*` peut être remplacé en spécifiant explicitement ` $ *`objet`*=` avec la valeur souhaitée.

La variable de chemin prédéfinie est généralement utilisée conjointement avec `template=`.

## Par défaut {#section-b02483d15529444586a2e9504805b155}

Aucun. Seules les variables qui ont été définies sont remplacées par le serveur (à l’exception de la variable de chemin prédéfinie $object, qui est toujours remplacée). Toutes les occurrences de ` $ *`var`*$` rester littéral si `*`var`*`ne peut pas être associé à une définition de variable existante.

## Exemples {#section-fba9393df6984247b7e30b3f93992e86}

Voir &quot;Exemple A&quot; dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
