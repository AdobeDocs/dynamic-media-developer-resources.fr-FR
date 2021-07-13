---
description: Les macros de commande fournissent des raccourcis nommés pour les jeux de commandes. Les macros sont définies dans des fichiers de définition de macro distincts, qui peuvent être joints aux catalogues d’images ou au catalogue par défaut.
solution: Experience Manager
title: Macros de commande
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# Macros de commande{#command-macros}

Les macros de commande fournissent des raccourcis nommés pour les jeux de commandes. Les macros sont définies dans des fichiers de définition de macro distincts, qui peuvent être joints aux catalogues d’images ou au catalogue par défaut.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>Nom de la macro. </p></td> 
 </tr> 
</table>

`*`Le nom `*`  n’est pas sensible à la casse et peut se composer de n’importe quelle combinaison de lettres ASCII, nombres , &#39;-&#39;, &#39;_&#39; et &#39;.&#39; caractères.

Les macros peuvent être invoquées n’importe où dans une requête après &quot;?&quot;, ainsi que n’importe où dans un champ `catalog::Modifier` ou `catalog::PostModifier`. Les macros ne peuvent représenter qu’une ou plusieurs commandes de diffusion d’images complètes et doivent être séparées des autres commandes avec les séparateurs &quot;&amp;&quot;.

Les appels de macro sont remplacés par leurs chaînes de substitution tôt lors de l’analyse. Les commandes des macros remplacent les mêmes commandes de la requête si elles se produisent avant l’appel de macro dans la requête. Ceci est différent de `catalog::Modifier`, où les commandes de la chaîne de requête remplacent toujours les commandes de la chaîne `catalog::Modifier`, quelle que soit la position dans la requête.

Les macros de commande ne peuvent pas comporter de valeurs d’argument, mais des variables personnalisées peuvent être utilisées pour transmettre des valeurs de la requête dans la macro.

Les macros peuvent être imbriquées, avec la restriction suivante : Une macro ne peut être appelée que si elle est déjà définie au moment de l’analyse de la définition de macro, soit en apparaissant plus tôt dans le même fichier de définition de macro, soit en plaçant la définition d’une telle macro incorporée dans le fichier de définition de macro par défaut.

## Exemple {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Les macros peuvent s’avérer utiles si les mêmes attributs doivent être appliqués à différentes images.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Nous pouvons définir une macro pour les attributs communs :

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

La macro sera utilisée comme suit :

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Dans la mesure où `wid=` est différent pour la troisième requête, nous remplaçons simplement la valeur *after* la macro est appelée (la spécification de `wid=`*before* `$view$` n’aurait aucun effet).

## Voir aussi {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalogue ::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [catalogue ::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), référence de  [définition de macro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
