---
description: Élément de modèle d’expression régulier. Facultatif dans les éléments <rule>.
solution: Experience Manager
title: expression
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---


# expression{#expression}

Élément de modèle d’expression régulier. Facultatif dans les éléments `<rule>`.

## Attributs {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Aucune

## Données {#section-e2601008d71243109af1a8c55b58416d}

Chaîne de modèle d’expression régulière.

## Description {#section-759bfb738ddb45dba1f0807aba8c1113}

L&#39;élément `<expression>` peut être vide ou contenir une chaîne de recherche simple ou un modèle d&#39;expression normal. Le modèle est appliqué à la chaîne de requête entière.

Une correspondance se produit toujours lorsque `<expression>` est vide ou non spécifié ; cela équivaut à spécifier `<expression>.*</expression>`.

L’implémentation est basée sur le package Java [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), qui fournit une syntaxe d’expression régulière similaire à celle de Perl.

## Remarques {#section-10b472a902674893b49ca49a7052c366}

La chaîne d&#39;expression ne doit pas contenir de caractères littéraux &lt; et &amp;. Ces caractères réservés peuvent être codés avec `&` et `<`, respectivement, ou la chaîne entière peut être incluse dans une section XML `CDATA` :

`<expression><![CDATA[&fmt=custom]]></expression>`

Tous les caractères compris entre les balises `<expression>` et `</expression>` sont transmis à l’analyseur d’expressions standard, y compris les caractères en dehors de la section facultative `CDATA`. Il faut prendre soin d’éviter les espaces blancs supplémentaires.

## Voir aussi {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
