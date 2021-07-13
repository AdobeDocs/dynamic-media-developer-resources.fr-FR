---
description: Les macros de commande fournissent des raccourcis nommés pour les jeux de commandes.
solution: Experience Manager
title: Macros de commande
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Macros de commande{#command-macros}

Les macros de commande fournissent des raccourcis nommés pour les jeux de commandes.

Les macros sont définies dans des fichiers de définition de macro distincts, qui peuvent être joints aux catalogues d’images ou au catalogue par défaut.

Les macros peuvent être invoquées n’importe où dans une requête après &quot;?&quot;, ainsi que n’importe où dans un champ `catalog::Modifier`. Les macros ne peuvent représenter qu’une ou plusieurs commandes de diffusion d’images complètes. Elles doivent donc être entourées des séparateurs &quot;&amp;&quot; (sauf au début ou à la fin de la chaîne de modification).

Les appels de macro sont remplacés par leurs chaînes de substitution tôt lors de l’analyse. Les commandes des macros remplacent les mêmes commandes de la requête si elles se produisent avant l’appel de macro dans la requête. Ceci est différent de `catalog::Modifier`, où les commandes de la chaîne de requête remplacent toujours les commandes de la chaîne `catalog::Modifier`, quelle que soit la position dans la requête.

Les macros peuvent être imbriquées, avec la restriction suivante : une macro ne peut être appelée que si elle est déjà définie au moment de l’analyse de la définition de macro, soit en apparaissant plus tôt dans le même fichier de définition de macro, soit en plaçant la définition d’une telle macro incorporée dans le fichier de définition de macro par défaut.

Les macros peuvent s’avérer utiles si les mêmes attributs doivent être appliqués à différentes images.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

Nous pouvons définir une macro pour les attributs communs :

`view wid=240&fmt=pdf&imageRes=300`

La macro sera utilisée comme suit :

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Dans la mesure où `wid=` est différent pour la troisième requête, nous remplaçons simplement la valeur *after* la macro est appelée (la spécification de `wid=`*before* `$view$` n’aurait aucun effet).

+ [name](r-name.md)
