---
description: Elément de modèle d’expression régulière. Facultatif dans <rule> les éléments.</rule>
solution: Experience Manager
title: expression
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---

# expression{#expression}

Elément de modèle d’expression régulière. Facultatif dans les `<rule>` éléments.

## Attributs {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Aucune

## Données {#section-e2601008d71243109af1a8c55b58416d}

Chaîne de modèle d’expression régulière.

## Description {#section-759bfb738ddb45dba1f0807aba8c1113}

L’élément `<expression>` peut être vide ou contenir une chaîne de recherche simple ou un modèle d’expression régulière. Le modèle est appliqué à l’intégralité de la chaîne de requête.

Une correspondance se produit toujours lorsque `<expression>` est vide ou non spécifié ; cela revient à spécifier `<expression>.*</expression>`.

L’implémentation est basée sur le paquet [Java java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), qui fournit une syntaxe d’expression régulière similaire à celle de Perl.

## Remarques {#section-10b472a902674893b49ca49a7052c366}

La chaîne d’expression ne doit pas contenir de littéral &lt; and &amp; characters. Ces caractères réservés peuvent être codés avec `&` et `<`, respectivement, ou la chaîne entière peut être incluse dans une section XML `CDATA` :

`<expression><![CDATA[&fmt=custom]]></expression>`

Tous les caractères entre les balises et `<expression>` `</expression>` sont transmis à l’analyseur d’expression régulière, y compris les caractères en dehors de la section facultative `CDATA` . Il faut veiller à éviter les espaces blancs supplémentaires.

## Voir aussi {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
