---
description: La diffusion d’images prend en charge un mécanisme de prétraitement des requêtes simple basé sur les règles de correspondance et de substitution des expressions régulières.
solution: Experience Manager
title: Référence d’ensemble de règles
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# Référence d’ensemble de règles{#rule-set-reference}

La diffusion d’images prend en charge un mécanisme de prétraitement des requêtes simple basé sur les règles de correspondance et de substitution des expressions régulières.

Collections de règles de prétraitement (*ensembles de règles*) peut être joint aux catalogues d’images ou au catalogue par défaut. Les règles du catalogue par défaut s’appliquent uniquement si la requête n’identifie pas un catalogue d’images principal spécifique.

Les règles de prétraitement des requêtes peuvent modifier les parties de chemin et de requête des requêtes avant qu’elles ne soient traitées par l’analyseur du serveur Platform, notamment en manipulant le chemin, en ajoutant des commandes, en modifiant les valeurs de commande et en appliquant des modèles ou des macros. Des règles peuvent également être utilisées pour configurer et remplacer certaines fonctionnalités de sécurité qui sont normalement contrôlées uniquement avec des attributs de catalogue, comme l’obscurcissement des demandes, le marquage à l’eau, ainsi que la limitation du service à des adresses IP client spécifiques.

Les ensembles de règles sont stockés sous la forme de fichiers de document XML. Le chemin relatif ou absolu du fichier d’ensemble de règles doit être spécifié dans `attribute::RuleSetFile`.

## Structure générale {#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
<ruleset> 
   <rule> 
      <expression> 
<varname>
  expression 
</varname></expression> 
      <substitution> 
<varname>
  substitution 
</varname></substitution> 
      <addressfilter> 
<varname>
  addressFilter 
</varname></addressfilter> 
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

Le `<?xml>` et `<ruleset>` Les éléments sont toujours requis dans un fichier XML de jeu de règles valide, même si aucune règle réelle n’est définie.

One `<ruleset>` élément contenant n’importe quel nombre `<rule>` sont autorisés.

Le contenu des fichiers de règles de prétraitement est sensible à la casse.

## Validation des jeux de règles {#section-d8d101a0b4d74580835e37d128d05567}

Une copie de [!DNL RuleSet.xsd] est fourni dans le dossier de catalogue et doit être utilisé pour valider un fichier d’ensemble de règles avant de l’enregistrer dans la variable [!DNL catalog.ini] fichier . Notez que le serveur d’images utilise une copie interne de [!DNL RuleSet.xsd] pour la validation.

## Prétraitement des URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Avant tout autre traitement, une requête HTTP entrante est partiellement analysée afin de déterminer quel catalogue d’images doit être appliqué. Une fois le catalogue identifié, le jeu de règles pour le catalogue sélectionné (ou le catalogue par défaut, si aucun catalogue spécifique n’a été identifié) est appliqué.

Le `<rule>` La recherche des éléments s’effectue dans l’ordre spécifié pour une correspondance avec le contenu de la variable `<expression>` element ( *`expression`*).

Si une `<rule>` est mis en correspondance, le paramètre facultatif *`substitution`* est appliquée et la chaîne de requête modifiée est transmise à l’analyseur de requêtes du serveur pour un traitement normal.

Si aucune correspondance réussie n’est effectuée lorsque la fin de la variable `<ruleset>` est atteinte, la requête est transmise à l’analyseur sans modification.

## Attribut OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

Le comportement par défaut peut être modifié à l’aide de la fonction `OnMatch` de l’attribut `<rule>` élément . `OnMatch` peut être défini sur `break` (par défaut), `continue`ou `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Elément et attribut</b> </th> 
   <th class="entry"> <b>Comportement lorsqu’une correspondance se produit</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>Le traitement des règles est arrêté immédiatement après l’application de la substitution de cette règle. Par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>La substitution est appliquée et le traitement se poursuit avec la règle suivante. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>Le traitement de la règle est arrêté immédiatement et un état de réponse "demande refusée" est renvoyé au client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remplacement des attributs de catalogue {#section-3f1e33a65c5346d1b4a69958c61432f3}

Le `rule` peut éventuellement définir des attributs qui remplacent les attributs de catalogue correspondants lorsque la règle est correctement mise en correspondance. Si plusieurs règles correspondantes définissent le même attribut, le dernier l’emporte. Voir [règle](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md) pour une liste d’attributs pouvant être contrôlés par des règles.

## Expressions régulières {#section-3f77bb9a265147b38c645f63ab1bad8b}

Une correspondance de chaîne simple fonctionne pour les applications très basiques, mais des expressions régulières sont requises dans la plupart des cas. Bien que les expressions régulières soient standard dans le secteur, l’implémentation spécifique varie d’une instance à l’autre.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) décrit l’implémentation spécifique des expressions régulières utilisée par le serveur d’images.

## Sous-chaînes capturées {#section-066e659406d5403599cd26ae35e80d68}

Pour faciliter des modifications d’URL complexes, les sous-chaînes peuvent être capturées dans l’expression en encadrant la sous-chaîne avec des parenthèses (..). Les sous-chaînes capturées sont numérotées de manière séquentielle, en commençant par 1, selon la position de la parenthèse de début. Les sous-chaînes capturées peuvent être insérées dans la substitution à l’aide de la fonction ` $ *`n`*`où *`n`* est le numéro de séquence de la sous-chaîne capturée.

## Gestion des fichiers de jeu de règles {#section-0598a608e4044bb4805fe93ceebe10a9}

Un fichier d’ensemble de règles peut être joint à chaque catalogue d’images avec l’attribut catalog `attribute::RuleSetFile`. Bien que vous puissiez modifier le fichier d’ensemble de règles à tout moment, le serveur d’images ne reconnaît les modifications que lorsque le catalogue d’images associé est rechargé. Ce rechargement se produit au démarrage ou au redémarrage du serveur de plateforme et chaque fois que le Principal fichier catalogue, qui comporte une [!DNL .ini] suffixe du fichier, est modifié ou &quot;touché&quot; pour modifier la date du fichier.

## Exemples {#section-aa769437d967459299b83a4bf34fe924}

**Exemple A.** Définissez une règle qui augmente les paramètres de qualité de l’image si le nom de l’image porte le suffixe &quot; [!DNL _hg]&quot;:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

L’expression de règle spécifie une correspondance non sensible à la casse de &quot; [!DNL _hg]&quot; à la fin de la chaîne d’URL. Le suffixe est remplacé par la chaîne de requête spécifiée qui modifie les paramètres de qualité de l’image. Notez que la variable `?` dans la chaîne de substitution est échappé car il s’agit d’un caractère spécial dans les expressions régulières.

>[!NOTE]
>
>Codage requis pour le caractère esperluette. Une autre solution consiste à placer la chaîne de substitution dans un bloc CDATA :

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Exemple B.** Une application web particulière n’autorise pas les chaînes de requête. Définir une règle qui convertit l’élément de chemin d’accès de fin `small`, `medium`ou `large` à un modèle, en utilisant le reste du chemin comme nom de l’image. Par exemple : `myCat/myImage/small` traduirait en `myCat/smallTemplate?src=myCat/myImage`.

Nous pouvons utiliser des sous-chaînes pour restructurer la requête :

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Voir aussi {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
