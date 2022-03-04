---
title: Variables personnalisées
description: La partie requête des requêtes et les chaînes de modificateur de vignette peuvent inclure des variables définies par l’utilisateur.
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

La partie requête des requêtes et la vignette ::Chaînes de modificateur peuvent inclure des variables définies par l’utilisateur.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Nom de variable. Peut se composer de n’importe quelle combinaison de caractères alpha, de chiffres et de caractères sûrs, à l’exclusion de `$`.

`[!DNL value]` - Valeur à laquelle la variable doit être définie (chaîne).

Les variables sont définies de la même manière que les autres commandes du serveur, à l’aide de la syntaxe ci-dessus. Les variables doivent être définies avant de pouvoir être référencées. Variables définies dans `vignette::Modifier` peut être référencé dans la requête d’URL, et inversement.

>[!NOTE]
>
>`[!DNL value]` doit être codé URL à un seul passage pour une transmission HTTP sécurisée. Un codage double est requis si `[!DNL value]` est retransmis par HTTP. C’est le cas lorsque `[!DNL value]` est remplacé par une requête étrangère imbriquée.

Les variables sont référencées en incorporant le nom de la variable (encadré d’un début et d’une fin). `$`) n’importe où dans les valeurs de commande. Par exemple, entre la variable `=`  en suivant le nom de la commande et les `&` ou la fin de la requête. Le serveur remplace chacune de ces occurrences de `$ [!DNL name]$` avec `[!DNL string]`. Il n’y a aucune substitution sur les occurrences de `$ [!DNL name]$` dans les noms de commande (avant le signe égal d’une commande) et dans la partie chemin de la requête.

Les variables personnalisées peuvent ne pas être imbriquées. Toutes les occurrences de `$ [!DNL name]$` dans `[!DNL string]` ne sont pas substituées. Par exemple, le fragment de requête `$var2=apple&$var1=my$var2$tree&text=$var1$` est résolu sur `text=my$var2$tree`.

`$` n’est pas un caractère réservé ; il peut se produire autrement dans la requête. Par exemple : `src=my$texture$file.tif` est une commande valide (en supposant qu’une entrée de catalogue de matières ou un fichier de texture nommé `[!DNL my$texture$file.tif]` existe), alors que `wid=$number$` n’est pas , car `wid=` nécessite un argument numérique.
