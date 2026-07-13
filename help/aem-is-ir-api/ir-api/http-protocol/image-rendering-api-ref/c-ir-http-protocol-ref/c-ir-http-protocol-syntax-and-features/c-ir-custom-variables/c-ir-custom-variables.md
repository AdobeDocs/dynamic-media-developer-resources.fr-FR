---
title: Variables personnalisées
description: La partie requête des requêtes et les chaînes du modificateur de vignette peuvent inclure des variables définies par l’utilisateur.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
TQID: 'https://experienceleague.adobe.com/1-o3GqgzwvPYV8UDBuZu5udOiG-p8Tue3Fo-ft8-QhI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 251
ht-degree: 0%

---

# Variables personnalisées{#custom-variables}

La partie requête des requêtes et les chaînes vignette::Modifier peuvent inclure des variables définies par l’utilisateur.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Nom de la variable. Peut consister en n’importe quelle combinaison de caractères alphanumériques, de chiffres et de caractères sécurisés, à l’exclusion de `$`.

`[!DNL value]` - Valeur pour laquelle la variable doit être définie (chaîne).

Les variables sont définies de la même manière que les autres commandes de serveur, en utilisant la syntaxe ci-dessus. Les variables doivent être définies avant de pouvoir être référencées. Les variables définies dans `vignette::Modifier` peuvent être référencées dans la requête d’URL, et inversement.

>[!NOTE]
>
>`[!DNL value]` doit être codé URL en une seule passe pour une transmission HTTP sécurisée. Un double encodage est requis si `[!DNL value]` est retransmis par le biais du protocole HTTP. C’est le cas lorsque la `[!DNL value]` est remplacée par une requête étrangère imbriquée.

Les variables sont référencées en incorporant le nom de la variable (entouré d’un `$` de début et d’un de fin) n’importe où dans les valeurs de commande. Par exemple, entre le `=` suivant le nom de la commande et le `&` suivant ou la fin de la requête. Le serveur remplace chaque occurrence de `$ [!DNL name]$` par `[!DNL string]`. Aucune substitution n’a lieu sur les occurrences de `$ [!DNL name]$` dans les noms de commande (avant le signe égal d’une commande) et dans la partie de chemin de la requête.

Les variables personnalisées ne peuvent pas être imbriquées. Les occurrences de `$ [!DNL name]$` dans `[!DNL string]` ne sont pas remplacées. Par exemple, le fragment de requête est `$var2=apple&$var1=my$var2$tree&text=$var1$` résolu sur `text=my$var2$tree`.

`$` n’est pas un caractère réservé ; il peut se produire autrement dans la requête. Par exemple, `src=my$texture$file.tif` est une commande valide (en supposant qu&#39;il existe une entrée de catalogue de matières ou un fichier de texture nommé `[!DNL my$texture$file.tif]`), alors que `wid=$number$` ne l&#39;est pas, car `wid=` requiert un argument numérique.

