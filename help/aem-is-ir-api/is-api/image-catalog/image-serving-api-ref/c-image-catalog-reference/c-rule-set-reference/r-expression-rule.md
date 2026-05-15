---
description: Élément de modèle d’expression régulière. Facultatif dans les éléments <rule>.
solution: Experience Manager
title: expression
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
TQID: 'https://experienceleague.adobe.com/lYaMuefBswTJcGuSm7Rm-yNTpz1UbOkjJLpdCOdXNrQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 3%

---

# expression{#expression}

Élément de modèle d’expression régulière. Facultatif dans les éléments `<rule>`.

## Attributs {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Aucune

## Données {#section-e2601008d71243109af1a8c55b58416d}

Chaîne de modèle d’expression régulière.

## Description {#section-759bfb738ddb45dba1f0807aba8c1113}

L’élément `<expression>` peut être vide ou contenir une simple chaîne de recherche ou un modèle d’expression régulière. Le modèle est appliqué à l’ensemble de la chaîne de requête.

Une correspondance se produit toujours lorsque `<expression>` est vide ou non spécifié ; cela équivaut à spécifier `<expression>.*</expression>`.

L’implémentation de repose sur le package Java [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), qui fournit une syntaxe d’expression régulière similaire à celle de Perl.

## Remarques {#section-10b472a902674893b49ca49a7052c366}

La chaîne d’expression ne doit pas contenir de caractères littéraux &lt; et &amp;. Ces caractères réservés peuvent être codés avec `&` et `<`, respectivement, ou l’ensemble de la chaîne peut être placé entre une section de `CDATA` XML :

`<expression><![CDATA[&fmt=custom]]></expression>`

Tous les caractères compris entre les balises `<expression>` et `</expression>` sont transmis à l’analyseur d’expression régulière, y compris les caractères en dehors de la section de `CDATA` facultative. Veillez à éviter les espaces supplémentaires.

## Voir aussi {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
