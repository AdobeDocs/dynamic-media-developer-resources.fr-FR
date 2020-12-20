---
description: Elément de chaîne de substitution. Facultatif dans les éléments <rule>.
seo-description: Elément de chaîne de substitution. Facultatif dans les éléments <rule>.
seo-title: substitution
solution: Experience Manager
title: substitution
topic: Scene7 Image Serving - Image Rendering API
uuid: f72902b1-0b0f-4401-9c3c-46573048cb25
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
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
