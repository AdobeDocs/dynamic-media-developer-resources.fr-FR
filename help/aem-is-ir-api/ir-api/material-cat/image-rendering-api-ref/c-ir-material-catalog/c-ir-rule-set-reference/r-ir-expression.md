---
description: Élément de modèle d’expression régulière. Facultatif dans les éléments <rule> .
solution: Experience Manager
title: expression
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 3%

---

# expression{#expression}

Élément de modèle d’expression régulière. Facultatif dans les éléments `<rule>`.

## Attributs {#section-fd0574eee1f9423cbb2ed709c0906800}

Aucune

## Données {#section-4cd740c511a1432da0955e9acfbcf96f}

Chaîne de modèle d’expression régulière.

## Description {#section-3245c8a531bb455d8398449f6ea63b37}

L’élément `<expression>` peut être vide ou contenir une simple chaîne de recherche ou un modèle d’expression régulière. Le modèle est appliqué à l’intégralité de la chaîne de requête.

Une correspondance se produit toujours lorsque `<expression>` est vide ou non spécifié ; cela équivaut à spécifier `<expression>.*</expression>`.

L’implémentation est basée sur le package Java [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), qui fournit une syntaxe d’expression régulière similaire à celle de Perl.

## Note {#section-6b41a900b0ce4a9590e5861e3c81599c}

La chaîne d’expression ne doit pas contenir de caractères littéraux &lt; et &amp; . Ces caractères réservés peuvent être codés respectivement avec `&` et `<` ou toute la chaîne peut être incluse dans une section `CDATA` XML :

`<expression><![CDATA[&fmt=custom]]></expression>`

Tous les caractères compris entre les balises `<expression>` et `</expression>` sont transmis à l’analyseur d’expressions régulières, y compris les caractères qui se trouvent en dehors de la section `CDATA` facultative. Soyez prudent afin d’éviter des espaces blancs supplémentaires.

## Voir aussi {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
