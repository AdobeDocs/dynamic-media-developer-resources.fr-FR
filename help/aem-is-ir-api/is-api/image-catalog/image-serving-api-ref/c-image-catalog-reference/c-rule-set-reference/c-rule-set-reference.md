---
description: Image Serving prend en charge un mécanisme de prétraitement de requête simple, basé sur des règles de correspondance et de substitution  et régulières.
seo-description: Image Serving prend en charge un mécanisme de prétraitement de requête simple, basé sur des règles de correspondance et de substitution  et régulières.
seo-title: Référence du jeu de règles
solution: Experience Manager
title: Référence du jeu de règles
topic: Scene7 Image Serving - Image Rendering API
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# Référence du jeu de règles{#rule-set-reference}

Image Serving prend en charge un mécanisme de prétraitement de requête simple, basé sur des règles de correspondance et de substitution  et régulières.

Les collections de règles de prétraitement (jeux *de* règles) peuvent être jointes aux catalogues d’images ou au catalogue par défaut. Les règles du catalogue par défaut s’appliquent uniquement si la requête n’identifie pas un catalogue d’images principal spécifique.

Les règles de prétraitement des requêtes peuvent modifier le chemin et  parties de requêtes avant d’être traitées par l’analyseur du serveur de plateformes, y compris la manipulation du chemin, l’ajout de commandes, la modification des valeurs de commande et l’application de modèles ou de macros. Des règles peuvent également être utilisées pour configurer et remplacer certaines fonctionnalités de sécurité qui sont normalement contrôlées uniquement avec des attributs de catalogue, comme l’obscurcissement de requête, le marquage à l’eau et la limitation du service à des adresses IP client spécifiques.

Les jeux de règles sont stockés sous la forme de fichiers  XML. Le chemin relatif ou absolu du fichier du jeu de règles doit être spécifié dans `attribute::RuleSetFile`.

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

Les éléments `<?xml>` et `<ruleset>` sont toujours requis dans un fichier XML de jeu de règles valide, même si aucune règle réelle n’est définie.

Un `<ruleset>` élément contenant un nombre quelconque d’ `<rule>` éléments est autorisé.

Le contenu des fichiers de règles de prétraitement est sensible à la casse.

## Validation des règles {#section-d8d101a0b4d74580835e37d128d05567}

Une copie de [!DNL RuleSet.xsd] est fournie dans le dossier du catalogue et doit être utilisée pour valider un fichier d’ensemble de règles avant de l’enregistrer dans le [!DNL catalog.ini] fichier. Notez que le serveur d’images utilise une copie interne de [!DNL RuleSet.xsd] pour la validation.

## Prétraitement des URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Avant tout autre traitement, une requête HTTP entrante est partiellement analysée afin de déterminer quel catalogue d’images doit être appliqué. Une fois le catalogue identifié, le jeu de règles pour le catalogue sélectionné (ou le catalogue par défaut, si aucun catalogue spécifique n’a été identifié) est appliqué.

Les `<rule>` éléments sont recherchés dans l’ordre spécifié pour une correspondance avec le contenu de l’ `<expression>` élément ( *`expression`*).

Si une correspondance `<rule>` est établie, le paramètre facultatif *`substitution`* est appliqué et la chaîne de requête modifiée est transmise à l’analyseur de requêtes du serveur pour un traitement normal.

Si aucune correspondance n’est établie lorsque la fin de la `<ruleset>` requête est atteinte, la requête est transmise à l’analyseur sans modification.

## Attribut OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

Le comportement par défaut peut être modifié avec l’ `OnMatch` attribut de l’ `<rule>` élément. `OnMatch` peut être définie sur `break` (par défaut), `continue`ou `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Elément et attribut</b> </th> 
   <th class="entry"> <b>Comportement en cas de correspondance</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;règle OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>Le traitement des règles est arrêté immédiatement après l’application de la substitution de cette règle. Par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;règle OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>La substitution est appliquée et le traitement se poursuit avec la règle suivante. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>Le traitement des règles est immédiatement interrompu et un état de réponse "demande refusée" est renvoyé au client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remplacement des attributs de catalogue {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` peuvent éventuellement définir des attributs qui remplacent les attributs de catalogue correspondants lorsque la règle est correctement mise en correspondance. Si plusieurs règles de correspondance définissent le même attribut, le dernier prévaut. Reportez-vous à la description de l’ ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` élément pour un d’attributs pouvant être contrôlés avec des règles.

##  régulier {#section-3f77bb9a265147b38c645f63ab1bad8b}

La correspondance simple des chaînes fonctionne pour des applications très basiques, mais des   régulières sont requises dans la plupart des cas. Bien que les   réguliers soient des normes du secteur, l’implémentation spécifique varie d’une instance à l’autre.

[ Le [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) décrit l’implémentation  régulière spécifique de l’ de utilisée par Image Serving.

## Sous-chaînes capturées {#section-066e659406d5403599cd26ae35e80d68}

Pour faciliter des modifications complexes des URL, il est possible de capturer des sous-chaînes dans le   en les encadrant de parenthèses (...). Les sous-chaînes capturées sont numérotées de manière séquentielle, en commençant par 1 selon la position de la parenthèse de début. Les sous-chaînes capturées peuvent être insérées dans la substitution à l’aide de ` $ *`n`*`, où *`n`* correspond au numéro de séquence de la sous-chaîne capturée.

## Gestion des fichiers de jeux de règles {#section-0598a608e4044bb4805fe93ceebe10a9}

Un fichier de jeu de règles peut être joint à chaque catalogue d’images avec l’attribut de catalogue `attribute::RuleSetFile`. Bien que vous puissiez modifier le fichier du jeu de règles à tout moment, le serveur d’images ne reconnaît les modifications que lorsque le catalogue d’images associé est rechargé. Ce rechargement se produit lorsque le serveur de plate-forme est démarré ou redémarré et lorsque le fichier de catalogue principal, qui comporte un suffixe de [!DNL .ini] fichier, est modifié ou &quot;touché&quot; pour modifier la date du fichier.

## Exemples {#section-aa769437d967459299b83a4bf34fe924}

**Exemple A.** Définissez une règle qui augmente les paramètres de qualité de l’image si le nom de l’image a le suffixe &quot; [!DNL _hg]&quot; :

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

La règle  le  spécifie une correspondance non sensible à la casse de &quot; [!DNL _hg]&quot; à la fin de la chaîne URL. Le suffixe est remplacé par la chaîne de  de spécifiée qui modifie les paramètres de qualité de l’image. Notez que le `?` caractère de la chaîne de substitution est ignoré car il s’agit d’un caractère spécial dans les   ordinaires.

>[!NOTE]
>
>Codage requis pour le caractère d’esperluette. Une autre solution consiste à placer la chaîne de substitution dans un bloc CDATA :

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Exemple B.** Une application Web particulière n’autorise pas les chaînes de . Définissez une règle qui traduit l’élément de chemin de fin `small`, `medium`ou `large` vers un modèle, en utilisant le reste du chemin comme nom d’image. Par exemple, `myCat/myImage/small` traduirait en `myCat/smallTemplate?src=myCat/myImage`.

Nous pouvons utiliser des sous-chaînes pour restructurer la requête :

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Voir aussi {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
