---
description: Élément de modèle -régulier . Facultatif dans les éléments <rule>.
seo-description: Élément de modèle -régulier . Facultatif dans les éléments <rule>.
seo-title: ' '
solution: Experience Manager
title: ' '
topic: Scene7 Image Serving - Image Rendering API
uuid: e7ef3769-0090-42d6-8021-1c213f1ee391
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# expression{#expression}

Élément de modèle -régulier . Facultatif dans `<rule>` les éléments.

## Attributes {#section-fd0574eee1f9423cbb2ed709c0906800}

Aucune

## Données {#section-4cd740c511a1432da0955e9acfbcf96f}

Chaîne de modèle de  régulière .

## Description {#section-3245c8a531bb455d8398449f6ea63b37}

L’ `<expression>` élément peut être vide ou contenir une chaîne de recherche simple ou un modèle de normal-. Le modèle est appliqué à la chaîne de requête entière.

Une correspondance se produit toujours lorsque `<expression>` est vide ou non spécifié ; cela équivaut à spécifier `<expression>.*</expression>`.

L’implémentation est basée sur le package Java [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), qui fournit une syntaxe de   régulière similaire à celle de Perl.

## Note {#section-6b41a900b0ce4a9590e5861e3c81599c}

La chaîne   ne doit pas contenir de caractères littéraux &lt; et &amp;. Ces caractères réservés peuvent être codés avec `&` et `<`, respectivement, ou la chaîne entière peut être incluse dans une `CDATA` section XML :

`<expression><![CDATA[&fmt=custom]]></expression>`

Tous les caractères compris entre les `<expression>` balises `</expression>` et sont transmis à l’analyseur  de classique, y compris les caractères qui se trouvent en dehors de la `CDATA` section facultative. Il faut prendre soin d’éviter les espaces blancs supplémentaires.

## Voir aussi {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
