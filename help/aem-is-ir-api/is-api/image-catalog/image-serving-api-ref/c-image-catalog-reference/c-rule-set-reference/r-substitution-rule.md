---
description: Elément Chaîne de substitution. Facultatif dans les éléments <rule> .
solution: Experience Manager
title: substitution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# substitution{#substitution}

Elément Chaîne de substitution. Facultatif dans les éléments `<rule>`.

## Attributs {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Aucune

## Données {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Chaîne de substitution.

## Description {#section-4a64a93f5e1a4d04a2db19166578bf76}

Définit une chaîne de remplacement pour la chaîne ou la sous-chaîne correspondante dans le chemin d’accès ou la requête.

Si l’expression de modèle inclut des sous-expressions (délimitées par des parenthèses), la première sous-chaîne correspondante est remplacée par la chaîne de substitution. Si l’expression de modèle n’inclut pas de sous-expressions, la chaîne correspondante entière est remplacée.

Si `<expression>` est vide ou absent, la chaîne de substitution est ajoutée au chemin ou à la requête.

Si `<substitution>` est vide, la chaîne ou la sous-chaîne correspondante est supprimée. Si `<substitution>` n’est pas spécifié, le chemin ou la chaîne de requête n’est pas modifié.

>[!NOTE]
>
>Toutes les correspondances dans la chaîne d’entrée sont remplacées lorsque `replace="all"` est spécifié dans l’élément `<rule>` auquel appartient cet élément `<substitution>`. Par défaut, seule la première correspondance est remplacée par la chaîne de substitution.

## Note {#section-cedf2adabaaf441c9f598fb0ea180246}

La chaîne de substitution ne doit pas contenir de caractères littéraux &lt; et &amp; . Ces caractères réservés peuvent être codés respectivement avec `&` et `<` ou toute la chaîne peut être incluse dans une section CDATA XML :

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
