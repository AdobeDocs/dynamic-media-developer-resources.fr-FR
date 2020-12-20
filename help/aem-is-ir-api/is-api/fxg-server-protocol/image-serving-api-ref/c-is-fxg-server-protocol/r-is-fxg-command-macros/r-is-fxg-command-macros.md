---
description: Les macros de commande fournissent des raccourcis nommés pour les jeux de commandes.
seo-description: Les macros de commande fournissent des raccourcis nommés pour les jeux de commandes.
seo-title: Macros de commande
solution: Experience Manager
title: Macros de commande
topic: Scene7 Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 4169757880407b62addd0a70ef1807d8b195820b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# macros de commande{#command-macros}

Les macros de commande fournissent des raccourcis nommés pour les jeux de commandes.

Les macros sont définies dans des fichiers de définition de macro distincts, qui peuvent être joints aux catalogues d’images ou au catalogue par défaut.

Les macros peuvent être invoquées n’importe où dans une requête après &quot;?&quot;, ainsi que n’importe où dans un champ `catalog::Modifier`. Les macros ne peuvent représenter qu’une ou plusieurs commandes complètes de traitement d’images, elles doivent donc être entourées de séparateurs &quot;&amp;&quot; (sauf lorsqu’elles se trouvent au début ou à la fin de la chaîne de modificateur).

Les appels de macros sont remplacés par leurs chaînes de substitution au début de l’analyse. Les commandes des macros remplacent les mêmes commandes dans la requête si elles surviennent avant l’appel de macro dans la requête. Ceci est différent de `catalog::Modifier`, où les commandes de la chaîne de requête remplacent toujours les commandes de la chaîne `catalog::Modifier`, quelle que soit la position de la requête.

Les macros peuvent être imbriquées avec la restriction suivante : une macro ne peut être appelée que si elle est déjà définie au moment de l&#39;analyse de la définition de macro, soit en apparaissant plus tôt dans le même fichier de définition de macro, soit en plaçant la définition d&#39;une telle macro incorporée dans le fichier de définition de macro par défaut.

Les macros peuvent s’avérer utiles si les mêmes attributs doivent être appliqués à des images différentes.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

Nous pouvons définir une macro pour les attributs communs :

`view wid=240&fmt=pdf&imageRes=300`

La macro serait utilisée comme suit :

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Comme `wid=` est différent pour la troisième requête, nous remplaçons simplement la valeur *après* l&#39;appel de la macro (la spécification de `wid=`*avant* `$view$` n&#39;aurait aucun effet).

+ [name](r-name.md)
