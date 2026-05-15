---
title: Macros de commande
description: Les macros de commande fournissent des raccourcis nommés pour des ensembles de commandes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
TQID: 'https://experienceleague.adobe.com/DbXn35KC7OLFI0Dulgobj3UFPHnubmCisNDS541j8lE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 248
ht-degree: 0%

---

# Macros de commande{#command-macros}

Les macros de commande fournissent des raccourcis nommés pour des ensembles de commandes.

Les macros sont définies dans des fichiers de définition de macro distincts, qui peuvent être joints aux catalogues d’images ou au catalogue par défaut.

Les macros peuvent être appelées n’importe où dans une requête après le caractère « ? » et n’importe où dans un champ de `catalog::Modifier`. Les macros ne peuvent représenter qu’une ou plusieurs commandes de diffusion d’images complètes. Par conséquent, elles doivent être entourées de séparateurs «&amp; » (sauf au début ou à la fin de la chaîne de modification).

Les appels de macro sont remplacés par leurs chaînes de substitution plus tôt pendant l’analyse. Les commandes contenues dans les macros remplacent les mêmes commandes dans la requête si elles se produisent avant l’appel de la macro dans la requête. Ce flux est différent du `catalog::Modifier`, où les commandes de la chaîne de requête remplacent toujours les commandes de la chaîne de `catalog::Modifier`, quelle que soit la position dans la requête.

Les macros peuvent être imbriquées. Cependant, une macro ne peut être appelée que si elle est déjà définie au moment de l&#39;analyse de la définition de macro. Ce flux est réalisé soit en apparaissant plus tôt dans le même fichier de définition de macro, soit en plaçant la définition d&#39;une telle macro incorporée dans le fichier de définition de macro par défaut.

Les macros peuvent s’avérer utiles si les mêmes attributs doivent être appliqués à différentes images.

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

Vous pouvez définir une macro pour les attributs communs :

`view wid=240&fmt=pdf&imageRes=300`

La macro serait utilisée comme suit :

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

Étant donné que `wid=` est différent pour la troisième requête, vous remplacez simplement la valeur *après* la macro est appelée (en spécifiant `wid=` *avant* `$view$` n’a aucun effet).

+ [nom](r-name.md)
