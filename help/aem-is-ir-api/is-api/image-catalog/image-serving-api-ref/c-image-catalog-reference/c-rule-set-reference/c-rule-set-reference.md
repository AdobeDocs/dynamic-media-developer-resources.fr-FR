---
description: La diffusion d’images prend en charge un mécanisme de prétraitement des demandes simple basé sur des règles de correspondance et de substitution d’expressions régulières.
solution: Experience Manager
title: Référence du jeu de règles
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
TQID: 'https://experienceleague.adobe.com/ZRyGq2UXh41F4IpGudN48CV0LxzrDjZKk2yaOQnUP3o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 808
ht-degree: 0%

---

# Référence du jeu de règles{#rule-set-reference}

La diffusion d’images prend en charge un mécanisme de prétraitement des demandes simple basé sur des règles de correspondance et de substitution d’expressions régulières.

Des collections de règles de pré-traitement (*ensembles de règles*) peuvent être jointes aux catalogues d’images ou au catalogue par défaut. Les règles du catalogue par défaut s’appliquent uniquement si la requête n’identifie pas un catalogue d’images principal spécifique.

Les règles de pré-traitement des requêtes peuvent modifier le chemin et les parties de requête des requêtes avant qu’elles ne soient traitées par l’analyseur du [!DNL Platform Server], notamment la manipulation du chemin, l’ajout de commandes, la modification des valeurs de commande et l’application de modèles ou de macros. Les règles peuvent également être utilisées pour configurer et remplacer certaines fonctionnalités de sécurité qui ne sont normalement contrôlées qu’avec des attributs de catalogue, tels que l’obscurcissement des requêtes, le filigrane, ainsi que pour limiter le service à des adresses IP client spécifiques.

Les ensembles de règles sont stockés en tant que fichiers de document XML. Le chemin d’accès relatif ou absolu du fichier d’ensemble de règles doit être spécifié dans `attribute::RuleSetFile`.

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

Les éléments `<?xml>` et `<ruleset>` sont toujours requis dans un fichier XML d’ensemble de règles valide, même si aucune règle réelle n’est définie.

Un élément `<ruleset>` contenant un nombre illimité d’éléments `<rule>` est autorisé.

Le contenu des fichiers de règles de prétraitement est sensible à la casse.

## Validation de l’ensemble de règles {#section-d8d101a0b4d74580835e37d128d05567}

Une copie de [!DNL RuleSet.xsd] est fournie dans le dossier de catalogue et doit être utilisée pour valider un fichier d’ensemble de règles avant de l’enregistrer dans le fichier de [!DNL catalog.ini]. Notez que la diffusion d’images utilise une copie interne de [!DNL RuleSet.xsd] pour la validation.

## Pré-traitement des URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Avant tout autre traitement, une requête HTTP entrante est partiellement analysée pour déterminer le catalogue d’images à appliquer. Une fois le catalogue identifié, le jeu de règles du catalogue sélectionné (ou du catalogue par défaut, si aucun catalogue spécifique n’a été identifié) est appliqué.

Les éléments `<rule>` sont recherchés dans l’ordre spécifié pour une correspondance avec le contenu de l’élément `<expression>` ( *`expression`*).

Si une `<rule>` est mise en correspondance, la *`substitution`* facultative est appliquée et la chaîne de requête modifiée est transmise à l’analyseur de requêtes du serveur pour un traitement normal.

Si aucune correspondance réussie n’est établie lorsque la fin de la `<ruleset>` est atteinte, la requête est transmise à l’analyseur sans modification.

## Attribut OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

Le comportement par défaut peut être modifié avec l’attribut `OnMatch` de l’élément `<rule>`. `OnMatch` peut être défini sur `break` (par défaut), `continue` ou `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Élément et attribut</b> </th> 
   <th class="entry"> <b>Comportement en cas de correspondance</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch=« break »&gt; </span> </p> </td> 
   <td> <p>Le traitement de la règle est arrêté immédiatement après l’application de la substitution de cette règle. Valeur par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch=« continue »&gt; </span> </p> </td> 
   <td> <p>La substitution est appliquée et le traitement se poursuit avec la règle suivante. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch=« error »&gt; </span> </p> </td> 
   <td> <p>Le traitement de la règle est immédiatement arrêté et un statut de réponse « demande refusée » est renvoyé au client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remplacement des attributs de catalogue {#section-3f1e33a65c5346d1b4a69958c61432f3}

L’élément `rule` peut éventuellement définir des attributs qui remplacent les attributs de catalogue correspondants lorsque la règle correspond. Si plusieurs règles correspondantes définissent le même attribut, la dernière prévaut. Voir l’élément [rule](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md) pour obtenir une liste d’attributs pouvant être contrôlés par des règles.

## Expressions régulières {#section-3f77bb9a265147b38c645f63ab1bad8b}

La correspondance de chaînes simple fonctionne pour les applications très basiques, mais les expressions régulières sont requises dans la plupart des instances. Bien que les expressions régulières soient standard, l’implémentation spécifique varie d’une instance à l’autre.

[[!DNL package java.util.regex]](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) décrit l’implémentation spécifique des expressions régulières utilisée par le service d’images.

## Sous-chaînes capturées {#section-066e659406d5403599cd26ae35e80d68}

Pour faciliter les modifications d’URL complexes, des sous-chaînes peuvent être capturées dans l’expression en plaçant la sous-chaîne entre parenthèses (...). Les sous-chaînes capturées sont numérotées de manière séquentielle en commençant par 1 selon la position de la parenthèse ouvrante. Les sous-chaînes capturées peuvent être insérées dans la substitution en utilisant ` $ *`n`*`, où *`n`* est le numéro de séquence de la sous-chaîne capturée.

## Gestion des fichiers d’ensemble de règles {#section-0598a608e4044bb4805fe93ceebe10a9}

Un fichier d’ensemble de règles peut être joint à chaque catalogue d’images avec l’attribut de catalogue `attribute::RuleSetFile`. Vous pouvez modifier le fichier d’ensemble de règles à tout moment, mais le serveur d’images ne reconnaît les modifications que lorsque le catalogue d’images associé est rechargé. Ce rechargement se produit lorsque le serveur de la plateforme est démarré ou redémarré et lorsque le fichier de catalogue principal, qui comporte un suffixe de fichier [!DNL .ini], est modifié ou « touché » pour modifier la date du fichier.

## Exemples {#section-aa769437d967459299b83a4bf34fe924}

**Exemple A.** Définissez une règle qui augmente les paramètres de qualité d’image si le nom de l’image porte le suffixe « [!DNL _hg] » :

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

L’expression de la règle spécifie une correspondance non sensible à la casse de « [!DNL _hg] » à la fin de la chaîne d’URL. Le suffixe est remplacé par la chaîne de requête spécifiée, ce qui modifie les paramètres de qualité d’image. Notez que le caractère `?` de la chaîne de substitution est placé dans une séquence d’échappement, car il s’agit d’un caractère spécial dans les expressions régulières.

>[!NOTE]
>
>Encodage requis pour l’esperluette. Alternativement, la chaîne de substitution peut être incluse dans un bloc CDATA :

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Exemple B.** Une application web spécifique n’autorise pas les chaînes de requête. Définissez une règle qui traduit l’élément de chemin de fin `small`, `medium` ou `large` en modèle, en utilisant le reste du chemin comme nom d’image. Par exemple, `myCat/myImage/small` se traduirait par `myCat/smallTemplate?src=myCat/myImage`.

Nous pouvons utiliser des sous-chaînes pour restructurer la requête :

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Voir aussi {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
