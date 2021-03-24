---
description: Élément de modèle d’expression régulière. Facultatif dans les éléments <rule>.
solution: Experience Manager
title: expression
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---


# expression{#expression}

Élément de modèle d’expression régulière. Facultatif dans les éléments `<rule>`.

## Attributs {#section-fd0574eee1f9423cbb2ed709c0906800}

Aucune

## Données {#section-4cd740c511a1432da0955e9acfbcf96f}

Chaîne de modèle d’expression régulière.

## Description {#section-3245c8a531bb455d8398449f6ea63b37}

L&#39;élément `<expression>` peut être vide ou contenir une chaîne de recherche simple ou un modèle d&#39;expression normal. Le modèle est appliqué à la chaîne de requête entière.

Une correspondance se produit toujours lorsque `<expression>` est vide ou non spécifié ; cela équivaut à spécifier `<expression>.*</expression>`.

L’implémentation est basée sur le package Java [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), qui fournit une syntaxe d’expression régulière similaire à celle de Perl.

## Note {#section-6b41a900b0ce4a9590e5861e3c81599c}

La chaîne d&#39;expression ne doit pas contenir de caractères littéraux &lt; et &amp;. Ces caractères réservés peuvent être codés avec `&` et `<`, respectivement, ou la chaîne entière peut être incluse dans une section XML `CDATA` :

`<expression><![CDATA[&fmt=custom]]></expression>`

Tous les caractères compris entre les balises `<expression>` et `</expression>` sont transmis à l’analyseur d’expressions standard, y compris les caractères en dehors de la section facultative `CDATA`. Il faut prendre soin d’éviter les espaces blancs supplémentaires.

## Voir aussi {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
