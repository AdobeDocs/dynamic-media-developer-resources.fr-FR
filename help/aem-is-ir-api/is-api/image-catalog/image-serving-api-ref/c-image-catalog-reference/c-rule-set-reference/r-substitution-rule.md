---
description: Élément de chaîne de substitution. Facultatif dans les éléments <rule>.
solution: Experience Manager
title: substitution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
TQID: 'https://experienceleague.adobe.com/ZdC23CxEXKYN0d-h7nM8588KTS5Vy6BTh0kl5Iseq0w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 1%

---

# substitution{#substitution}

Élément de chaîne de substitution. Facultatif dans les éléments `<rule>`.

## Attributs {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Aucune

## Données {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Chaîne de substitution.

## Description {#section-4a64a93f5e1a4d04a2db19166578bf76}

Définit une chaîne de remplacement pour la chaîne ou sous-chaîne correspondante dans le chemin d’accès ou la requête.

Si l’expression de modèle comprend des sous-expressions (délimitées par des parenthèses), la première sous-chaîne correspondante est remplacée par la chaîne de substitution. Si l’expression de modèle n’inclut pas de sous-expressions, l’intégralité de la chaîne correspondante est remplacée.

Si `<expression>` est vide ou absent, la chaîne de substitution est ajoutée au chemin d’accès ou à la requête.

Si `<substitution>` est vide, la chaîne ou sous-chaîne correspondante est supprimée. Si `<substitution>` n’est pas spécifié, le chemin d’accès ou la chaîne de requête n’est pas modifié.

>[!NOTE]
>
>Toutes les correspondances de la chaîne d’entrée sont remplacées lorsque `replace="all"` est spécifié dans l’élément `<rule>`,à laquelle cet élément `<substitution>` appartient. Par défaut, seule la première correspondance est remplacée par la chaîne de substitution.

## Note {#section-cedf2adabaaf441c9f598fb0ea180246}

La chaîne de substitution ne doit pas contenir de caractères littéraux &lt; et &amp;. Ces caractères réservés peuvent être codés avec `&` et `<`, respectivement, ou la chaîne entière peut être placée entre crochets dans une section XML CDATA :

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
