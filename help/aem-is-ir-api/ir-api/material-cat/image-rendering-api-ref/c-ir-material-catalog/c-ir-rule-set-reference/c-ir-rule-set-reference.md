---
description: Le rendu d’image prend en charge un mécanisme de prétraitement de requête simple, basé sur des règles de correspondance et de substitution  et régulières.
seo-description: Le rendu d’image prend en charge un mécanisme de prétraitement de requête simple, basé sur des règles de correspondance et de substitution  et régulières.
seo-title: Référence du jeu de règles
solution: Experience Manager
title: Référence du jeu de règles
topic: Scene7 Image Serving - Image Rendering API
uuid: aeec7597-4d23-4cf8-8bdc-3a133152eadb
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# Référence du jeu de règles{#rule-set-reference}

Le rendu d’image prend en charge un mécanisme de prétraitement de requête simple, basé sur des règles de correspondance et de substitution  et régulières.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Les collections de règles de prétraitement (jeux *de* règles) peuvent être jointes aux catalogues de matières ou au catalogue par défaut. Les règles du catalogue par défaut s’appliquent uniquement si la requête ne joint pas un catalogue de matières spécifique.

Les règles de prétraitement des requêtes peuvent modifier le chemin et  parties de requêtes avant d’être traitées par l’analyseur de requêtes du serveur, notamment en manipulant le chemin d’accès, en ajoutant des commandes, en modifiant les valeurs de commande et en appliquant des modèles ou des macros. Des règles peuvent également être utilisées pour configurer et remplacer certains attributs de catalogue, ainsi que pour limiter le service à des adresses IP client spécifiques.

Les jeux de règles sont stockés sous la forme de fichiers  XML. Le chemin relatif ou absolu du fichier du jeu de règles doit être spécifié dans `attribute::RuleSetFile`.

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

Les éléments `<?xml>`, `<!DOCTYPE>` et `<ruleset>` sont toujours requis dans un fichier XML de jeu de règles valide, même si aucune règle réelle n’est définie.

Un `<ruleset>` élément contenant un nombre quelconque d’ `<rule>` éléments est autorisé.

Le contenu des fichiers de règles de prétraitement est sensible à la casse.

## Prétraitement des URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Avant tout autre traitement, une requête HTTP entrante est partiellement analysée afin de déterminer le catalogue matériel à appliquer. Une fois le catalogue identifié, le jeu de règles pour le catalogue sélectionné (ou le catalogue par défaut, si aucun catalogue spécifique n’a été identifié) est appliqué.

Les `<rule>` éléments sont recherchés dans l’ordre spécifié pour une correspondance avec le contenu de l’ `<expression>` élément ( *`expression`*).

Si une correspondance `<rule>` est établie, le paramètre facultatif *`substitution`* est appliqué et la chaîne de requête modifiée est transmise à l’analyseur de requêtes du serveur pour un traitement normal.

Si aucune correspondance n’est établie lorsque la fin de la `<ruleset>` requête est atteinte, la requête est transmise à l’analyseur sans modification.

## Attribut OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

Le comportement par défaut peut être modifié avec l’ `OnMatch` attribut des `<rule>` éléments. `OnMatch` peut être définie sur `break` (par défaut), `continue`ou `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Elément et attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Comportement en cas de correspondance </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;règle OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Le traitement des règles est arrêté immédiatement après l’application de la substitution de cette règle. Par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;règle OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>La substitution est appliquée et le traitement se poursuit avec la règle suivante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Le traitement des règles est immédiatement interrompu et un état de réponse "demande refusée" est renvoyé au client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remplacement des attributs de catalogue {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` peuvent éventuellement définir des attributs qui remplacent les attributs de catalogue correspondants lorsque la règle est correctement mise en correspondance et `OnMatch="break"` définie. Aucun attribut n’est appliqué si `OnMatch="continue"` est défini. Reportez-vous à la description d’ `<rule>` un d’attributs pouvant être contrôlés avec des règles.

##  régulier {#section-4d326507b52544b0960a9a5f303e3fe6}

La correspondance simple des chaînes fonctionne pour des applications très basiques, mais des   régulières sont requises dans la plupart des cas. Bien que les   réguliers soient des normes du secteur, l’implémentation spécifique varie d’une instance à l’autre.

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) décrit l’implémentation  régulière spécifique de  de utilisée par Image Serving.

## Sous-chaînes capturées {#section-8057cd65d48949ffb6a50e929bd3688b}

Pour faciliter des modifications complexes des URL, il est possible de capturer des sous-chaînes dans le   en les encadrant de parenthèses (...). Les sous-chaînes capturées sont numérotées de manière séquentielle, en commençant par 1 selon la position de la parenthèse de début. Les sous-chaînes capturées peuvent être insérées dans la substitution en utilisant *`$n`*, où *`n`* correspond au numéro de séquence de la sous-chaîne capturée.

## Gestion des fichiers de jeux de règles {#section-e8ce976b56404c009496426fd334d23d}

Un fichier de jeu de règles peut être joint à chaque catalogue de matières avec l’attribut de catalogue `attribute::RuleSetFile`. Bien que vous puissiez modifier le fichier du jeu de règles à tout moment, le serveur d’images ne reconnaît les modifications que lorsque le catalogue de matières associé est rechargé. Cela se produit lorsque le serveur de plateformes est démarré ou redémarré et lorsque le fichier catalogue principal (qui comporte un suffixe de [!DNL .ini] fichier) est modifié ou &quot;touché&quot; (pour modifier la date du fichier).

## Exemples {#section-c4142a41f5cd4ff799a72fbc130c3700}

Des exemples d’ensemble de règles sont fournis dans la section correspondante de la référence du catalogue d’images dans la documentation de la diffusion d’images.

## Voir aussi {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
