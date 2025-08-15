---
description: Image Rendering prend en charge un mécanisme de pré-traitement de requête simple basé sur des règles de correspondance et de substitution d’expressions régulières.
solution: Experience Manager
title: Référence d’ensemble de règles
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# Référence d’ensemble de règles{#rule-set-reference}

Image Rendering prend en charge un mécanisme de pré-traitement de requête simple basé sur des règles de correspondance et de substitution d’expressions régulières.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Des collections de règles de prétraitement (*ensembles* de règles) peuvent être attachées à des catalogues de matériaux ou au catalogue par défaut. Les règles du catalogue par défaut s’appliquent uniquement si la demande n’attache pas de catalogue de matériaux spécifique.

Les règles de prétraitement des demandes peuvent modifier les parties chemin d’accès et requête des requêtes avant qu’elles ne soient traitées par l’analyseur de requêtes du serveur, notamment en manipulant le chemin d’accès, en ajoutant des commandes, en modifiant les valeurs de commande et en appliquant des modèles ou des macros. Les règles peuvent également être utilisées pour configurer et remplacer certains attributs de catalogue, ainsi que pour limiter le service à des adresses IP client spécifiques.

Les ensembles de règles sont stockés en tant que fichiers de document XML. Le chemin d’accès relatif ou absolu du fichier de jeu de règles doit être spécifié dans `attribute::RuleSetFile`.

## Structure générale {#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
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
   </rule>
</ruleset>
```

Les `<?xml>`éléments et `<!DOCTYPE>` `<ruleset>` sont toujours requis dans un fichier XML de jeu de règles valide, même si aucune règle réelle n’est définie.

Un `<ruleset>` élément contenant un nombre quelconque d’éléments `<rule>` est autorisé.

Le contenu des fichiers de règles de prétraitement est sensible à la casse.

## Prétraitement des URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Avant tout autre traitement, une requête HTTP entrante est partiellement analysée pour déterminer quel catalogue de matériaux doit être appliqué. Une fois le catalogue identifié, le jeu de règles pour le catalogue sélectionné (ou le catalogue par défaut, si aucun catalogue spécifique n’a été identifié) est appliqué.

Les `<rule>` éléments sont recherchés dans l’ordre indiqué pour une correspondance avec le contenu de l’élément `<expression>` ( *`expression`*).

Si un correspond à un `<rule>` , l’option facultative *`substitution`* est appliquée et la chaîne de requête modifiée est transmise à l’analyseur de requêtes du serveur pour un traitement normal.

Si aucune correspondance n’est établie lorsque la fin de l’est `<ruleset>` atteinte, la demande est transmise à l’analyseur sans modification.

## Attribut OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

Le comportement par défaut peut être modifié avec l’attribut `OnMatch` des `<rule>` éléments. `OnMatch` peut être définie sur `break` (par défaut), `continue`, ou `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Elément et attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Comportement lorsqu’une correspondance se produit </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule onmatch="break"&gt;</span>&lt;/rule&gt; </p> </td> 
   <td colname="col2"> <p>Le traitement des règles est arrêté immédiatement après l’application de la substitution de cette règle. Faire défaut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule onmatch="continue"&gt;</span>&lt;/rule&gt; </p> </td> 
   <td colname="col2"> <p>La substitution est appliquée et le traitement se poursuit avec la règle suivante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule onmatch="error"&gt;</span>&lt;/rule&gt; </p> </td> 
   <td colname="col2"> <p>Le traitement des règles est arrêté immédiatement et un état de réponse « demande refusée » est renvoyé au client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remplacement des attributs de catalogue {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` Les éléments peuvent éventuellement définir des attributs qui remplacent les attributs de catalogue correspondants lorsque la règle est correctement mise en correspondance et `OnMatch="break"` définie. Aucun attribut n’est appliqué si `OnMatch="continue"` est défini. Reportez-vous à la description de `<rule>` pour obtenir la liste des attributs qui peuvent être contrôlés par des règles.

## Expressions régulières {#section-4d326507b52544b0960a9a5f303e3fe6}

La correspondance de chaînes simple fonctionne pour des applications très basiques, mais des expressions régulières sont requises dans la plupart des cas. Bien que les expressions régulières soient standard, l’implémentation spécifique varie d’une instance à l’autre.

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) décrit l’implémentation spécifique de l’expression régulière utilisée par le serveur d’images.

## Sous-chaînes capturées {#section-8057cd65d48949ffb6a50e929bd3688b}

Pour faciliter les modifications d’URL complexes, des sous-chaînes peuvent être capturées dans l’expression en la plaçant entre parenthèses (...). Les sous-chaînes capturées sont numérotées séquentiellement en commençant par 1 selon la position de la parenthèse principale. Les sous-chaînes capturées peuvent être insérées dans la substitution en utilisant *`$n`*, où *`n`* est le numéro de séquence de la sous-chaîne capturée.

## Gestion des fichiers de jeux de règles {#section-e8ce976b56404c009496426fd334d23d}

Un fichier d’ensemble de règles peut être joint à chaque catalogue de matériaux avec l’attribut `attribute::RuleSetFile`catalog . Bien que vous puissiez modifier le fichier d’ensemble de règles à tout moment, le serveur d’images reconnaît les modifications uniquement lorsque le catalogue de matériaux associé est rechargé. Cela se produit lorsque le [!DNL Platform Server] est démarré ou redémarré et chaque fois que le fichier catalogue principal (qui a un [!DNL .ini] suffixe de fichier) est modifié ou « touché » (pour changer la date du fichier).

## Exemples {#section-c4142a41f5cd4ff799a72fbc130c3700}

Des exemples d’ensemble de règles sont fournis dans la section correspondante de la référence du catalogue d’images de la documentation Image Server.

## Voir aussi {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[Package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
