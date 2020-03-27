---
description: Elément de chaîne de substitution. Facultatif dans les éléments <rule>.
seo-description: Elément de chaîne de substitution. Facultatif dans les éléments <rule>.
seo-title: substitution
solution: Experience Manager
title: substitution
topic: Scene7 Image Serving - Image Rendering API
uuid: e5730559-0512-4416-927d-a7faf9180741
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# substitution{#substitution}

Elément de chaîne de substitution. Facultatif dans `<rule>` les éléments.

## Attributes {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Aucune

## Données {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Chaîne de substitution.

## Description {#section-4a64a93f5e1a4d04a2db19166578bf76}

Définit une chaîne de remplacement pour la chaîne ou la sous-chaîne correspondante dans le chemin d’accès ou le  de.

Si le modèle   inclut un de sous- (délimité par des parenthèses), la première sous-chaîne correspondante est remplacée par la chaîne de substitution. Si le modèle   n’inclut pas de sous-, la chaîne correspondante entière est remplacée.

S’ `<expression>` il est vide ou absent, la chaîne de substitution est ajoutée au chemin d’accès ou au .

Si `<substitution>` est vide, la chaîne ou la sous-chaîne correspondante est supprimée. Si `<substitution>` n’est pas spécifié, le chemin d’accès ou la chaîne de  du ne sont pas modifiés.

>[!NOTE]
>
>Toutes les correspondances dans la chaîne d’entrée sont remplacées lorsque `replace="all"` elles sont spécifiées dans l’ `<rule>`,élément auquel cet `<substitution>` élément appartient. Par défaut, seule la première correspondance est remplacée par la chaîne de substitution.

## Note {#section-cedf2adabaaf441c9f598fb0ea180246}

La chaîne de substitution ne doit pas contenir de caractères littéraux &lt; et &amp;. Ces caractères réservés peuvent être codés avec `&` et `<`, respectivement, ou la chaîne entière peut être incluse dans une section CDATA XML :

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
