---
description: Elément Chaîne de substitution. Facultatif dans les éléments <rule> .
solution: Experience Manager
title: substitution
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---

# substitution{#substitution}

Elément Chaîne de substitution. Facultatif dans les éléments `<rule>`.

## Attributs {#section-d955eefc53eb4274861270669c01f9ca}

Aucune

## Données {#section-a2688866ed6d41279a8478886e511ae3}

Chaîne de substitution.

## Description {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Définit une chaîne de remplacement pour la chaîne ou la sous-chaîne correspondante dans le chemin d’accès ou la requête.

Si l’expression de modèle inclut des sous-expressions (délimitées par des parenthèses), la première sous-chaîne correspondante est remplacée par la chaîne de substitution. Si l’expression de modèle n’inclut pas de sous-expressions, la chaîne correspondante entière est remplacée.

Si `<expression>` est vide ou absent, la chaîne de substitution est ajoutée au chemin ou à la requête.

Si `<substitution>` est vide, la chaîne ou la sous-chaîne correspondante est supprimée. Si `<substitution>` n’est pas spécifié, le chemin d’accès ou la chaîne de requête n’est pas modifié.

## Note {#section-90fe89bb17a04804b7ff3c93df082892}

La chaîne de substitution ne doit pas contenir de caractères littéraux &lt; et &amp; . Ces caractères réservés peuvent être codés respectivement avec `&` et `<` ou toute la chaîne peut être incluse dans une section `CDATA` XML :

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
