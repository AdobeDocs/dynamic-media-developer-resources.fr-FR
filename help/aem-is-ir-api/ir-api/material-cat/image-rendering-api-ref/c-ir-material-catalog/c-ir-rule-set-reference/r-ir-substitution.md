---
title: substitution
description: Elément de chaîne de substitution. Facultatif dans <rule> les éléments.</rule>
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# substitution{#substitution}

Elément de chaîne de substitution. Facultatif dans les `<rule>` éléments.

## Attributs {#section-d955eefc53eb4274861270669c01f9ca}

Aucune

## Données {#section-a2688866ed6d41279a8478886e511ae3}

Chaîne de substitution.

## Description {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Définit une chaîne de remplacement pour la chaîne ou la sous-chaîne correspondante dans le chemin ou la requête.

Si l’expression de modèle inclut des sous-expressions (délimitées par des parenthèses), la première sous-chaîne correspondante est remplacée par la chaîne de substitution. Si l’expression du modèle n’inclut pas de sous-expressions, toute la chaîne correspondante est substituée.

Si `<expression>` la valeur est vide ou absente, la chaîne de substitution est ajoutée au chemin ou à la requête.

Si `<substitution>` est vide, la chaîne ou la sous-chaîne correspondante est supprimée. Si `<substitution>` n’est pas spécifié, le chemin d’accès ou la chaîne de requête ne sont pas modifiés.

## Note {#section-90fe89bb17a04804b7ff3c93df082892}

La chaîne de substitution ne doit pas contenir de littéral &lt; and &amp; characters. Ces caractères réservés peuvent être codés avec `&` et `<`, respectivement, ou la chaîne entière peut être incluse dans une section XML `CDATA` :

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
