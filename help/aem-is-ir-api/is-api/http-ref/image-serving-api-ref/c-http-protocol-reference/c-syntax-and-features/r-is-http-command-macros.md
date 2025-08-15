---
title: Macros de commande
description: Les macros de commande fournissent des raccourcis nommés pour des ensembles de commandes. Les macros sont définies dans des fichiers de définition de macro distincts, qui peuvent être joints aux catalogues d’images ou au catalogue par défaut.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Macros de commande{#command-macros}

Les macros de commande fournissent des raccourcis nommés pour des ensembles de commandes. Les macros sont définies dans des fichiers de définition de macro distincts, qui peuvent être joints aux catalogues d’images ou au catalogue par défaut.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nom</span></span> </p> </td> 
  <td class="stentry"> <p>Nom de la macro. </p></td> 
 </tr> 
</table>

`*`name`*` n’est pas sensible à la casse et peut consister en une combinaison de lettres ASCII, de chiffres , de caractères &#39;-&#39;, &#39;_&#39; et &#39;.&#39; caractères.

Les macros peuvent être appelées n’importe où dans une requête après le caractère « ? » et n’importe où dans un champ `catalog::Modifier` ou `catalog::PostModifier`. Les macros ne peuvent représenter qu’une ou plusieurs commandes de traitement d’images complètes et doivent être séparées des autres commandes avec des séparateurs de `&`.

Les appels de macro sont remplacés par leurs chaînes de substitution plus tôt pendant l’analyse. Les commandes contenues dans les macros remplacent les mêmes commandes dans la requête si elles se produisent avant l’appel de la macro dans la requête. Ce flux de traitement est différent du `catalog::Modifier`, où les commandes de la chaîne de requête remplacent toujours les commandes de la chaîne de `catalog::Modifier`, quelle que soit la position dans la requête.

Les macros de commande ne peuvent pas avoir de valeurs d’argument, mais des variables personnalisées peuvent être utilisées pour transmettre des valeurs de la requête dans la macro.

Les macros peuvent être imbriquées. Cependant, une macro ne peut être appelée que si elle est déjà définie au moment de l&#39;analyse de la définition de macro. Ce workflow est exécuté soit en apparaissant plus tôt dans le même fichier de définition de macro, soit en plaçant la définition d&#39;une macro incorporée dans le fichier de définition de macro par défaut.

## Exemple {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Les macros peuvent s’avérer utiles si les mêmes attributs doivent être appliqués à différentes images.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Vous pouvez définir une macro pour les attributs communs :

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

La macro serait utilisée comme suit :

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Étant donné que `wid=` est différent pour la troisième requête, vous pouvez simplement remplacer la valeur *après* la macro est appelée (la spécification de `wid=`*avant* `$view$` n’a aucun effet).

## Voir aussi {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [Référence de définition de macro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
