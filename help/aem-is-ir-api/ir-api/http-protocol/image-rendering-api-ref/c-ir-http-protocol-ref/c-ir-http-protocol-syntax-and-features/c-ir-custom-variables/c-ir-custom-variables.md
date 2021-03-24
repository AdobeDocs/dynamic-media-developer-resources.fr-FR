---
description: La partie requête des requêtes et les chaînes de modificateur de vignette peuvent inclure des variables définies par l’utilisateur.
solution: Experience Manager
title: Variables personnalisées
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---


# Variables personnalisées{#custom-variables}

La partie requête des requêtes et les chaînes vignette::Modificateur peuvent inclure des variables définies par l’utilisateur.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Nom de variable. Peut se composer de n’importe quelle combinaison de caractères alphabétiques, de chiffres et de caractères sûrs, à l’exclusion de &quot;$&quot;.

** *[!DNL value]* ** Valeur à laquelle la variable doit être définie (chaîne).

Les variables sont définies de la même manière que les autres commandes serveur, en utilisant la syntaxe ci-dessus. Les variables doivent être définies avant d’être référencées. Les variables définies dans `vignette::Modifier` peuvent être référencées dans la requête d’URL, et inversement.

>[!NOTE]
>
>*[!DNL value]* doit être codé en URL à un seul passage pour une transmission HTTP sécurisée. Un codage par doublon est requis si *[!DNL value]* est retransmis via HTTP. C’est le cas lorsque *[!DNL value]* est remplacé dans une requête étrangère imbriquée.

Les variables sont référencées en incorporant le nom de la variable (encadré par un $ de début et un $ de fin) n’importe où dans les valeurs de commande. Par exemple, entre &quot;=&quot; après le nom de la commande et &quot;&amp;&quot; suivant ou la fin de la requête. Le serveur remplace chaque occurrence de $ *[!DNL name]*$ par *[!DNL string]*. Aucune substitution n’est effectuée sur les occurrences de $ *[!DNL name]*$ dans les noms de commande (avant le signe égal d’une commande) et dans la partie chemin de la requête.

Il est possible que les variables personnalisées ne soient pas imbriquées. Les occurrences de $ *[!DNL name]*$ dans *[!DNL string]* ne sont pas remplacées. Par exemple, le fragment de requête `$var2=apple&$var1=my$var2$tree&text=$var1$` est résolu en `text=my$var2$tree`.

$ n’est pas un caractère réservé ; il peut se produire autrement dans la demande. Par exemple, `src=my$texture$file.tif` est une commande valide (en supposant qu&#39;il existe une entrée de catalogue de matières ou un fichier de texture nommé [!DNL my$texture$file.tif]), contrairement à `wid=$number$`, car `wid=` nécessite un argument numérique.
