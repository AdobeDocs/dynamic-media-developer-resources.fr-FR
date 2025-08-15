---
title: Macros de commande
description: Les macros de commandes fournissent des raccourcis nommés pour des ensembles de commandes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Macros de commande{#command-macros}

Les macros de commandes fournissent des raccourcis nommés pour des ensembles de commandes.

Les macros sont définies dans des fichiers de définition de macros distincts, qui peuvent être joints aux catalogues d’images ou au catalogue par défaut.

Les macros peuvent être invoquées n’importe où dans une requête après le « ? », et n’importe où dans un `catalog::Modifier` champ. Les macros ne peuvent représenter qu’une ou plusieurs commandes complètes de diffusion d’images, elles doivent donc être entourées de séparateurs &#39;&amp;&#39; (sauf au début ou à la fin de la chaîne de modificateur).

Les appels de macro sont remplacés par leurs chaînes de substitution au début de l’analyse. Les commandes dans les macros remplacent les mêmes commandes dans la demande si elles se produisent avant l’appel de macro dans la demande. Ce flux est différent de `catalog::Modifier`, où les commandes de la chaîne de requête remplacent toujours les commandes de la `catalog::Modifier` chaîne, quelle que soit la position dans la requête.

Les macros peuvent être imbriquées. Toutefois, une macro ne peut être appelée que si elle est déjà définie au moment de l’analyse de la définition de la macro. Ce flux est accompli soit en apparaissant précédemment dans le même fichier de définition de macro, soit en plaçant la définition d’une telle macro incorporée dans le fichier de définition de macro par défaut.

Les macros peuvent être utiles si les mêmes attributs doivent être appliqués à différentes images.

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

Vous pouvez définir une macro pour les attributs communs :

`view wid=240&fmt=pdf&imageRes=300`

L’utilisation de la macro se présente comme suit :

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

Comme `wid=` est différent pour la troisième requête, vous remplacez simplement la valeur *après* l’appel de la macro (spécifier `wid=` *avant* `$view$` n’a aucun effet).

+ [nom](r-name.md)
