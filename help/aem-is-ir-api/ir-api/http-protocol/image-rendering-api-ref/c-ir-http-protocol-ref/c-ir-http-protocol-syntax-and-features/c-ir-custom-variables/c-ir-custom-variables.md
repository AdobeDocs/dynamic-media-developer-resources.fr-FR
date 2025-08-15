---
title: Variables personnalisées
description: La partie requête des requêtes et des chaînes de modificateur de vignette peut inclure des variables définies par l’utilisateur.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Variables personnalisées{#custom-variables}

La partie requête des requêtes et des chaînes vignette ::Modifier peut inclure des variables définies par l’utilisateur.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Nom de la variable. Peut comprendre toute combinaison de caractères alphanumériques, numériques et de caractères sûrs, à l’exclusion du `$`.

`[!DNL value]` - Valeur sur laquelle la variable doit être définie (chaîne).

Les variables sont définies de la même manière que les autres commandes du serveur, à l’aide de la syntaxe ci-dessus. Les variables doivent être définies avant de pouvoir être référencées. Les variables définies dans `vignette::Modifier` peuvent être référencées dans la requête d’URL, et inversement.

>[!NOTE]
>
>`[!DNL value]` doit être codé en URL monopassage pour une transmission HTTP sécurisée. Un double encodage est requis si `[!DNL value]` est retransmis par le biais de HTTP. C’est le cas lorsque `[!DNL value]` est substitué à une demande étrangère imbriquée.

Les variables sont référencées en incorporant le nom de variable (entouré d’un début et d’un fin) `$`n’importe où dans les valeurs de commande. Par exemple, entre le nom de `=`  commande suivant et la suite `&` ou la fin de la requête. Le serveur remplace chacune de ces occurrences par `$ [!DNL name]$` `[!DNL string]`. Aucune substitution ne se produit sur les occurrences de dans les noms de `$ [!DNL name]$` commande (avant le signe égal d’une commande) et dans la partie chemin de la requête.

Les variables personnalisées ne peuvent pas être imbriquées. Les occurrences de `$ [!DNL name]$` dans `[!DNL string]` ne sont pas remplacées. Par exemple, le fragment `$var2=apple&$var1=my$var2$tree&text=$var1$` de requête est résolu sur `text=my$var2$tree`.

`$` n’est pas un caractère réservé ; il se peut qu’il en soit autrement dans la demande. Par exemple, `src=my$texture$file.tif` est une commande valide (en supposant qu’une entrée de catalogue de matériaux ou un fichier de texture nommé `[!DNL my$texture$file.tif]` existe), alors que `wid=$number$` ne l’est pas, car `wid=` nécessite un argument numérique.
