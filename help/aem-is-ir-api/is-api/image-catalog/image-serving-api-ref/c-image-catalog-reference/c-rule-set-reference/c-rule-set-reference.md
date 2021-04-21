---
description: La diffusion d’images prend en charge un mécanisme de prétraitement de requête simple, qui repose sur des règles de correspondance et de substitution d’expressions régulières.
solution: Experience Manager
title: Référence du jeu de règles
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---


# Référence du jeu de règles {#rule-set-reference}

La diffusion d’images prend en charge un mécanisme de prétraitement de requête simple, qui repose sur des règles de correspondance et de substitution d’expressions régulières.

Les collections de règles de prétraitement (*ensembles de règles*) peuvent être jointes aux catalogues d’images ou au catalogue par défaut. Les règles du catalogue par défaut s’appliquent uniquement si la demande n’identifie pas un catalogue d’images principal spécifique.

Les règles de prétraitement des requêtes peuvent modifier les parties chemin et requête des requêtes avant d’être traitées par l’analyseur du serveur de plateformes, notamment en manipulant le chemin, en ajoutant des commandes, en modifiant les valeurs de commande et en appliquant des modèles ou des macros. Des règles peuvent également être utilisées pour configurer et remplacer certaines fonctions de sécurité qui sont normalement contrôlées uniquement avec des attributs de catalogue, comme l&#39;obscurcissement des demandes, le marquage à l&#39;eau, ainsi que la limitation du service à des adresses IP client spécifiques.

Les jeux de règles sont stockés en tant que fichiers de document XML. Le chemin relatif ou absolu du fichier de jeu de règles doit être spécifié dans `attribute::RuleSetFile`.

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

Les éléments `<?xml>` et `<ruleset>` sont toujours requis dans un fichier XML de jeu de règles valide, même si aucune règle réelle n&#39;est définie.

Un élément `<ruleset>` contenant un nombre quelconque d&#39;éléments `<rule>` est autorisé.

Le contenu des fichiers de règles de prétraitement est sensible à la casse.

## Validation des ensembles de règles {#section-d8d101a0b4d74580835e37d128d05567}

Une copie de [!DNL RuleSet.xsd] est fournie dans le dossier catalogue et doit être utilisée pour valider un fichier d&#39;ensemble de règles avant de l&#39;enregistrer dans le fichier [!DNL catalog.ini]. Notez que la diffusion d’images utilise une copie interne de [!DNL RuleSet.xsd] pour validation.

## Prétraitement de l’URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Avant tout autre traitement, une requête HTTP entrante est partiellement analysée afin de déterminer quel catalogue d’images doit être appliqué. Une fois le catalogue identifié, le jeu de règles pour le catalogue sélectionné (ou le catalogue par défaut, si aucun catalogue spécifique n’a été identifié) est appliqué.

Les éléments `<rule>` sont recherchés dans l&#39;ordre spécifié pour une correspondance avec le contenu de l&#39;élément `<expression>` ( *`expression`*).

Si un `<rule>` correspond, le *`substitution`* facultatif est appliqué et la chaîne de requête modifiée est transmise à l’analyseur de requêtes du serveur pour traitement normal.

Si aucune correspondance réussie n&#39;est établie lorsque la fin de `<ruleset>` est atteinte, la requête est transmise à l&#39;analyseur sans modification.

## Attribut OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

Le comportement par défaut peut être modifié avec l&#39;attribut `OnMatch` de l&#39;élément `<rule>`. `OnMatch` peut être définie sur  `break` (par défaut),  `continue` ou  `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Elément et attribut</b> </th> 
   <th class="entry"> <b>Comportement en cas de correspondance</b> </th> 
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

`<rule>` peuvent éventuellement définir des attributs qui remplacent les attributs de catalogue correspondants lorsque la règle est correctement mise en correspondance. Si plusieurs règles de correspondance définissent le même attribut, le dernier l’emporte. Reportez-vous à la description de l&#39;élément ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` pour obtenir une liste d&#39;attributs qui peuvent être contrôlés avec des règles.

## Expressions régulières {#section-3f77bb9a265147b38c645f63ab1bad8b}

La simple correspondance des chaînes fonctionne pour les applications de base, mais des expressions régulières sont requises dans la plupart des cas. Bien que les expressions régulières soient conformes aux normes du secteur, la mise en oeuvre spécifique varie d’une instance à l’autre.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) décrit la mise en oeuvre d’expression régulière spécifique utilisée par Image Serving.

## Sous-chaînes capturées {#section-066e659406d5403599cd26ae35e80d68}

Pour faciliter des modifications d’URL complexes, les sous-chaînes peuvent être capturées dans l’expression en encadrant la sous-chaîne avec des parenthèses (...). Les sous-chaînes capturées sont numérotées de manière séquentielle en commençant par 1, en fonction de la position de la parenthèse de début. Les sous-chaînes capturées peuvent être insérées dans la substitution en utilisant ` $ *`n`*`, où *`n`* est le numéro de séquence de la sous-chaîne capturée.

## Gestion des fichiers de jeu de règles {#section-0598a608e4044bb4805fe93ceebe10a9}

Un fichier d&#39;ensemble de règles peut être joint à chaque catalogue d&#39;images avec l&#39;attribut de catalogue `attribute::RuleSetFile`. Bien que vous puissiez modifier le fichier du jeu de règles à tout moment, le serveur d’images ne reconnaît les modifications que lorsque le catalogue d’images associé est rechargé. Ce rechargement se produit lorsque le serveur de plate-forme est démarré ou redémarré et chaque fois que le fichier catalogue Principal, doté du suffixe [!DNL .ini], est modifié ou &quot;touché&quot; pour modifier la date du fichier.

## Exemples {#section-aa769437d967459299b83a4bf34fe924}

**Exemple A.** Définissez une règle qui augmente les paramètres de qualité de l’image si le nom de l’image a le suffixe &quot;  [!DNL _hg]&quot; :

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

L’expression de règle spécifie une correspondance non sensible à la casse de &quot; [!DNL _hg]&quot; à la fin de la chaîne d’URL. Le suffixe est remplacé par la chaîne de requête spécifiée qui modifie les paramètres de qualité de l’image. Notez que le caractère `?` de la chaîne de substitution est ignoré car il s’agit d’un caractère spécial dans les expressions régulières.

>[!NOTE]
>
>Codage requis pour le caractère esperluette. Une autre solution consiste à placer la chaîne de substitution dans un bloc CDATA :

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Exemple B.** Une application Web particulière n’autorise pas les chaînes de requête. Définissez une règle qui convertit l’élément de chemin de fin `small`, `medium` ou `large` en modèle, en utilisant le reste du chemin comme nom de l’image. Par exemple, `myCat/myImage/small` correspond à `myCat/smallTemplate?src=myCat/myImage`.

Nous pouvons utiliser des sous-chaînes pour restructurer la demande :

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Voir aussi {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
