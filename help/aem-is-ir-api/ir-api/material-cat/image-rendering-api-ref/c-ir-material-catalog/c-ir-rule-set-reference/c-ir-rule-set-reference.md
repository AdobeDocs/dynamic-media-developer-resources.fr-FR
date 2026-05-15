---
description: Le rendu des images prend en charge un mécanisme de pré-traitement des requêtes simple basé sur des règles de correspondance et de substitution d’expression régulière.
solution: Experience Manager
title: Référence du jeu de règles
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
TQID: 'https://experienceleague.adobe.com/HxgWcboIyA2RYuXbHMKaUiRQFL8IDNKegdOqMgz2plE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 642
ht-degree: 0%

---

# Référence du jeu de règles{#rule-set-reference}

Le rendu des images prend en charge un mécanisme de pré-traitement des requêtes simple basé sur des règles de correspondance et de substitution d’expression régulière.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Les collections de règles de pré-traitement (*ensembles de règles*) peuvent être associées aux catalogues de matières ou au catalogue par défaut. Les règles du catalogue par défaut ne s&#39;appliquent que si la demande ne joint pas de catalogue de matières spécifique.

Les règles de pré-traitement des requêtes peuvent modifier le chemin et les parties de requête des requêtes avant qu’elles ne soient traitées par l’analyseur de requêtes du serveur, notamment la manipulation du chemin, l’ajout de commandes, la modification des valeurs de commande et l’application de modèles ou de macros. Les règles peuvent également être utilisées pour configurer et remplacer certains attributs de catalogue, ainsi que pour limiter le service à des adresses IP clientes spécifiques.

Les ensembles de règles sont stockés en tant que fichiers de document XML. Le chemin d’accès relatif ou absolu du fichier d’ensemble de règles doit être spécifié dans `attribute::RuleSetFile`.

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

Un élément `<ruleset>` contenant un nombre illimité d’éléments `<rule>` est autorisé.

Le contenu des fichiers de règles de prétraitement est sensible à la casse.

## Pré-traitement des URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Avant tout autre traitement, une requête HTTP entrante est partiellement analysée afin de déterminer quel catalogue de matériaux doit être appliqué. Une fois le catalogue identifié, le jeu de règles du catalogue sélectionné (ou du catalogue par défaut, si aucun catalogue spécifique n’a été identifié) est appliqué.

Les éléments `<rule>` sont recherchés dans l’ordre spécifié pour une correspondance avec le contenu de l’élément `<expression>` ( *`expression`*).

Si une `<rule>` est mise en correspondance, la *`substitution`* facultative est appliquée et la chaîne de requête modifiée est transmise à l’analyseur de requêtes du serveur pour un traitement normal.

Si aucune correspondance réussie n’est établie lorsque la fin de la `<ruleset>` est atteinte, la requête est transmise à l’analyseur sans modification.

## Attribut OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

Le comportement par défaut peut être modifié avec l’attribut `OnMatch` des éléments `<rule>`. `OnMatch` peut être défini sur `break` (par défaut), `continue` ou `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Élément et attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Comportement en cas de correspondance </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch=« break »&gt;</span> </p> </td> 
   <td colname="col2"> <p>Le traitement de la règle est arrêté immédiatement après l’application de la substitution de cette règle. Valeur par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch=« continue »&gt;</span> </p> </td> 
   <td colname="col2"> <p>La substitution est appliquée et le traitement se poursuit avec la règle suivante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch=« error »&gt;</span> </p> </td> 
   <td colname="col2"> <p>Le traitement de la règle est immédiatement arrêté et un statut de réponse « demande refusée » est renvoyé au client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remplacement des attributs de catalogue {#section-1f59ce84234f4576ba8473b0e6ba22ee}

Les éléments `<rule>` peuvent éventuellement définir des attributs qui remplacent les attributs de catalogue correspondants lorsque la règle est correctement mise en correspondance et que `OnMatch="break"` est définie. Aucun attribut n’est appliqué si `OnMatch="continue"` est défini. Reportez-vous à la description de `<rule>` pour obtenir une liste des attributs qui peuvent être contrôlés avec des règles.

## Expressions régulières {#section-4d326507b52544b0960a9a5f303e3fe6}

La correspondance de chaînes simple fonctionne pour les applications très basiques, mais les expressions régulières sont requises dans la plupart des instances. Bien que les expressions régulières soient standard, l’implémentation spécifique varie d’une instance à l’autre.

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) décrit l’implémentation spécifique de l’expression régulière utilisée par la diffusion d’images.

## Sous-chaînes capturées {#section-8057cd65d48949ffb6a50e929bd3688b}

Pour faciliter les modifications d’URL complexes, des sous-chaînes peuvent être capturées dans l’expression en plaçant la sous-chaîne entre parenthèses (...). Les sous-chaînes capturées sont numérotées de manière séquentielle en commençant par 1 selon la position de la parenthèse ouvrante. Les sous-chaînes capturées peuvent être insérées dans la substitution à l&#39;aide de *`$n`*, où *`n`* est le numéro de séquence de la sous-chaîne capturée.

## Gestion des fichiers d’ensemble de règles {#section-e8ce976b56404c009496426fd334d23d}

Un fichier d&#39;ensemble de règles peut être joint à chaque catalogue de matières avec l&#39;attribut de catalogue `attribute::RuleSetFile`. Bien que vous puissiez modifier le fichier d&#39;ensemble de règles à tout moment, le serveur d&#39;images ne reconnaît les modifications que lorsque le catalogue de matériaux associé est rechargé. Cela se produit lorsque le [!DNL Platform Server] est démarré ou redémarré, et chaque fois que le fichier de catalogue principal (qui comporte un suffixe de fichier [!DNL .ini]) est modifié ou « touché » (pour modifier la date du fichier).

## Exemples {#section-c4142a41f5cd4ff799a72fbc130c3700}

Des exemples d’ensembles de règles sont fournis dans la section correspondante de la référence de catalogue d’images dans la documentation du service d’images.

## Voir aussi {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
