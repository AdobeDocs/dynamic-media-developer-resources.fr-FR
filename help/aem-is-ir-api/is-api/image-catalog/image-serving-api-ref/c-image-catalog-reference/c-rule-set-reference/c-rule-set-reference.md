---
description: Image Serving prend en charge un mécanisme de prétraitement de requête simple basé sur des règles de correspondance et de substitution d’expressions régulières.
solution: Experience Manager
title: Référence d’ensemble de règles
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Référence d’ensemble de règles{#rule-set-reference}

Image Serving prend en charge un mécanisme de prétraitement de requête simple basé sur des règles de correspondance et de substitution d’expressions régulières.

Des collections de règles de prétraitement (*ensembles* de règles) peuvent être attachées à des catalogues d’images ou au catalogue par défaut. Les règles du catalogue par défaut s’appliquent uniquement si la demande n’identifie pas de catalogue d’images principal spécifique.

Les règles de prétraitement des demandes peuvent modifier les parties chemin et requête des requêtes avant qu’elles ne soient traitées par l’analyseur [!DNL Platform Server]de , notamment en manipulant le chemin d’accès, en ajoutant des commandes, en modifiant les valeurs de commande et en appliquant des modèles ou des macros. Les règles peuvent également être utilisées pour configurer et remplacer certaines fonctionnalités de sécurité qui ne sont normalement contrôlées qu’avec des attributs de catalogue, telles que l’obscurcissement des demandes, le filigrane, ainsi que la limitation du service à des adresses IP client spécifiques.

Les ensembles de règles sont stockés en tant que fichiers de document XML. Le chemin d’accès relatif ou absolu du fichier de jeu de règles doit être spécifié dans `attribute::RuleSetFile`.

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

Les `<?xml>` éléments et `<ruleset>` sont toujours requis dans un fichier XML de jeu de règles valide, même si aucune règle réelle n’est définie.

Un `<ruleset>` élément contenant un nombre quelconque d’éléments `<rule>` est autorisé.

Le contenu des fichiers de règles de prétraitement est sensible à la casse.

## Validation de l’ensemble de règles {#section-d8d101a0b4d74580835e37d128d05567}

Une copie de [!DNL RuleSet.xsd] est fournie dans le dossier catalog et doit être utilisée pour valider un fichier d’ensemble de règles avant de l’enregistrer dans le [!DNL catalog.ini] fichier. Notez que le serveur d’images utilise une copie interne de [!DNL RuleSet.xsd] pour la validation.

## Prétraitement des URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Avant tout autre traitement, une requête HTTP entrante est partiellement analysée pour déterminer quel catalogue d’images doit être appliqué. Une fois le catalogue identifié, le jeu de règles pour le catalogue sélectionné (ou le catalogue par défaut, si aucun catalogue spécifique n’a été identifié) est appliqué.

Les `<rule>` éléments sont recherchés dans l’ordre indiqué pour une correspondance avec le contenu de l’élément `<expression>` ( *`expression`*).

Si un correspond à un `<rule>` , l’option facultative *`substitution`* est appliquée et la chaîne de requête modifiée est transmise à l’analyseur de requêtes du serveur pour un traitement normal.

Si aucune correspondance n’est établie lorsque la fin de l’est `<ruleset>` atteinte, la demande est transmise à l’analyseur sans modification.

## Attribut OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

Le comportement par défaut peut être modifié avec l’attribut `OnMatch` de l’élément `<rule>` . `OnMatch` peut être définie sur `break` (par défaut), `continue`, ou `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Elément et attribut</b> </th> 
   <th class="entry"> <b>Comportement lorsqu’une correspondance se produit</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">&lt;rule onmatch="break"&gt; </span>&lt;/rule&gt; </p> </td> 
   <td> <p>Le traitement des règles est arrêté immédiatement après l’application de la substitution de cette règle. Faire défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">&lt;rule onmatch="continue"&gt; </span>&lt;/rule&gt; </p> </td> 
   <td> <p>La substitution est appliquée et le traitement se poursuit avec la règle suivante. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">&lt;rule onmatch="error"&gt; </span>&lt;/rule&gt; </p> </td> 
   <td> <p>Le traitement des règles est arrêté immédiatement et un état de réponse « demande refusée » est renvoyé au client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remplacement des attributs de catalogue {#section-3f1e33a65c5346d1b4a69958c61432f3}

L’élément `rule` peut éventuellement définir des attributs qui remplacent les attributs de catalogue correspondants lorsque la règle est correctement mise en correspondance. Si plusieurs règles correspondantes définissent le même attribut, la dernière prévaut. Voir [Élément de règle](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md) pour obtenir la liste des attributs qui peuvent être contrôlés par des règles.

## Expressions régulières {#section-3f77bb9a265147b38c645f63ab1bad8b}

La correspondance de chaînes simple fonctionne pour des applications très basiques, mais des expressions régulières sont requises dans la plupart des cas. Bien que les expressions régulières soient standard, l’implémentation spécifique varie d’une instance à l’autre.

[[!DNL package java.util.regex]](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) décrit la mise en œuvre spécifique d’expressions régulières utilisée par le serveur d’images.

## Sous-chaînes capturées {#section-066e659406d5403599cd26ae35e80d68}

Pour faciliter les modifications d’URL complexes, des sous-chaînes peuvent être capturées dans l’expression en la plaçant entre parenthèses (...). Les sous-chaînes capturées sont numérotées séquentiellement en commençant par 1 selon la position de la parenthèse principale. Les sous-chaînes capturées peuvent être insérées dans la substitution en utilisant ` $ *`n, où `*` est *`n`* le numéro de séquence de la sous-chaîne capturée.

## Gestion des fichiers de jeux de règles {#section-0598a608e4044bb4805fe93ceebe10a9}

Un fichier d’ensemble de règles peut être joint à chaque catalogue d’images avec l’attribut `attribute::RuleSetFile`catalog . Bien que vous puissiez modifier le fichier d’ensemble de règles à tout moment, le serveur d’images reconnaît les modifications uniquement lorsque le catalogue d’images associé est rechargé. Ce rechargement se produit lorsque le serveur de plate-forme est démarré ou redémarré et chaque fois que le fichier catalogue principal, qui a un [!DNL .ini] suffixe de fichier, est modifié ou « touché » pour changer la date du fichier.

## Exemples {#section-aa769437d967459299b83a4bf34fe924}

**Exemple A.** Définir une règle qui augmente les paramètres de qualité de l’image si le nom de l’image a le suffixe &quot; [!DNL _hg]« :

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

L’expression de règle spécifie une correspondance sans distinction des majuscules et minuscules de &quot; [!DNL _hg]&quot; à la fin de la chaîne URL. Le suffixe est remplacé par la chaîne de requête spécifiée qui modifie les paramètres de qualité de l’image. Notez que le `?` caractère de la chaîne de substitution est échappé car il s’agit d’un caractère spécial dans les expressions régulières.

>[!NOTE]
>
>Codage requis pour le caractère esperluette. Sinon, la chaîne de substitution peut être incluse dans un bloc CDATA :

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Exemple B.** Une application Web particulière n’autorise pas les chaînes de requête. Définissez une règle qui traduit l’élément `small`de chemin de fin , `medium`ou `large` en un modèle, en utilisant le reste du chemin comme nom d’image. Par exemple, `myCat/myImage/small` se traduit par `myCat/smallTemplate?src=myCat/myImage`.

Nous pouvons utiliser des sous-chaînes pour restructurer la requête :

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Voir aussi {#section-9b748e7c5cff4759a70f96657bd43352}

[Package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
