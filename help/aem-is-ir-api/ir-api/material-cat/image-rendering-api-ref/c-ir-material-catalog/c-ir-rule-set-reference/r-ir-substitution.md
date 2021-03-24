---
description: Elément de chaîne de substitution. Facultatif dans les éléments <rule>.
solution: Experience Manager
title: substitution
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---


# substitution{#substitution}

Elément de chaîne de substitution. Facultatif dans les éléments `<rule>`.

## Attributs {#section-d955eefc53eb4274861270669c01f9ca}

Aucune

## Données {#section-a2688866ed6d41279a8478886e511ae3}

Chaîne de substitution.

## Description {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Définit une chaîne de remplacement pour la chaîne ou sous-chaîne correspondante dans le chemin d’accès ou la requête.

Si l’expression de modèle inclut des sous-expressions (délimitées par des parenthèses), la première sous-chaîne correspondante est remplacée par la chaîne de substitution. Si l’expression de modèle n’inclut pas de sous-expressions, la chaîne correspondante complète est remplacée.

Si `<expression>` est vide ou absent, la chaîne de substitution est ajoutée au chemin d’accès ou à la requête.

Si `<substitution>` est vide, la chaîne ou sous-chaîne correspondante est supprimée. Si `<substitution>` n&#39;est pas spécifié, le chemin d&#39;accès ou la chaîne de requête n&#39;est pas modifié.

## Note {#section-90fe89bb17a04804b7ff3c93df082892}

La chaîne de substitution ne doit pas contenir de caractères littéraux &lt; et &amp;. Ces caractères réservés peuvent être codés avec `&` et `<`, respectivement, ou la chaîne entière peut être incluse dans une section XML `CDATA` :

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
