---
description: Le rendu d’image prend en charge un mécanisme de prétraitement de requête simple basé sur les règles de correspondance et de substitution des expressions régulières.
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

Le rendu d’image prend en charge un mécanisme de prétraitement de requête simple basé sur les règles de correspondance et de substitution des expressions régulières.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Les collections de règles de prétraitement (*ensembles de règles*) peuvent être jointes à des catalogues de matériaux ou au catalogue par défaut. Les règles du catalogue par défaut ne s’appliquent que si la demande ne joint pas de catalogue de matières spécifique.

Les règles de prétraitement des requêtes peuvent modifier les parties de chemin et de requête des requêtes avant qu’elles ne soient traitées par l’analyseur de requêtes du serveur, notamment en manipulant le chemin, en ajoutant des commandes, en modifiant les valeurs de commande et en appliquant des modèles ou des macros. Des règles peuvent également être utilisées pour configurer et remplacer certains attributs de catalogue, ainsi que pour limiter le service à des adresses IP client spécifiques.

Les ensembles de règles sont stockés sous la forme de fichiers de document XML. Le chemin d’accès relatif ou absolu du fichier d’ensemble de règles doit être spécifié dans `attribute::RuleSetFile`.

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

Les éléments `<?xml>`, `<!DOCTYPE>` et `<ruleset>` sont toujours requis dans un fichier XML d’ensemble de règles valide, même si aucune règle réelle n’est définie.

Un élément `<ruleset>` contenant un nombre indéfini d&#39;éléments `<rule>` est autorisé.

Le contenu des fichiers de règles de prétraitement est sensible à la casse.

## Prétraitement des URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Avant tout autre traitement, une requête HTTP entrante est partiellement analysée afin de déterminer quel catalogue de matériaux doit être appliqué. Une fois le catalogue identifié, le jeu de règles pour le catalogue sélectionné (ou le catalogue par défaut, si aucun catalogue spécifique n’a été identifié) est appliqué.

Les éléments `<rule>` sont recherchés dans l’ordre spécifié pour une correspondance avec le contenu de l’élément `<expression>` ( *`expression`*).

Si un `<rule>` correspond, le *`substitution`* facultatif est appliqué et la chaîne de requête modifiée est transmise à l’analyseur de requêtes du serveur pour un traitement normal.

Si aucune correspondance réussie n’est effectuée lorsque la fin de `<ruleset>` est atteinte, la requête est transmise à l’analyseur sans modification.

## Attribut OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

Le comportement par défaut peut être modifié avec l’attribut `OnMatch` des éléments `<rule>` . `OnMatch` peut être défini sur `break` (par défaut), `continue` ou `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Elément et attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Comportement lorsqu’une correspondance se produit </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Le traitement des règles est arrêté immédiatement après l’application de la substitution de cette règle. Valeur par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>La substitution est appliquée et le traitement se poursuit avec la règle suivante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Le traitement de la règle est arrêté immédiatement et un état de réponse "demande refusée" est renvoyé au client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remplacement des attributs de catalogue {#section-1f59ce84234f4576ba8473b0e6ba22ee}

Les éléments `<rule>` peuvent éventuellement définir des attributs qui remplacent les attributs de catalogue correspondants lorsque la règle est correctement mise en correspondance et que `OnMatch="break"` est défini. Aucun attribut n’est appliqué si `OnMatch="continue"` est défini. Reportez-vous à la description de `<rule>` pour obtenir la liste des attributs qui peuvent être contrôlés avec des règles.

## Expressions régulières {#section-4d326507b52544b0960a9a5f303e3fe6}

Une correspondance de chaîne simple fonctionne pour les applications très basiques, mais des expressions régulières sont requises dans la plupart des cas. Bien que les expressions régulières soient standard dans le secteur, l’implémentation spécifique varie d’une instance à l’autre.

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) décrit l’implémentation spécifique des expressions régulières utilisée par le serveur d’images.

## Sous-chaînes capturées {#section-8057cd65d48949ffb6a50e929bd3688b}

Pour faciliter des modifications d’URL complexes, les sous-chaînes peuvent être capturées dans l’expression en encadrant la sous-chaîne avec des parenthèses (..). Les sous-chaînes capturées sont numérotées de manière séquentielle, en commençant par 1, selon la position de la parenthèse de début. Les sous-chaînes capturées peuvent être insérées dans la substitution en utilisant *`$n`*, où *`n`* est le numéro de séquence de la sous-chaîne capturée.

## Gestion des fichiers de jeu de règles {#section-e8ce976b56404c009496426fd334d23d}

Un fichier d&#39;ensemble de règles peut être joint à chaque catalogue de matières avec l&#39;attribut de catalogue `attribute::RuleSetFile`. Bien que vous puissiez modifier le fichier d’ensemble de règles à tout moment, le serveur d’images ne reconnaît les modifications que lorsque le catalogue de matériel associé est rechargé. Cela se produit lorsque le [!DNL Platform Server] est démarré ou redémarré et lorsque le fichier de catalogue principal (qui comporte un suffixe de fichier [!DNL .ini]) est modifié ou &quot;touché&quot; (pour modifier la date du fichier).

## Exemples {#section-c4142a41f5cd4ff799a72fbc130c3700}

Des exemples de jeux de règles sont fournis dans la section correspondante de la référence du catalogue d’images de la documentation du serveur d’images.

## Voir aussi {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
