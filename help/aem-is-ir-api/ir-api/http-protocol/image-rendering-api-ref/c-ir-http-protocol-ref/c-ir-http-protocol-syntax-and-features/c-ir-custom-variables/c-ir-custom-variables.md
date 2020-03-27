---
description: La partie des requêtes et les chaînes de modificateur de vignette peuvent inclure des variables définies par l’utilisateur.
seo-description: La partie des requêtes et les chaînes de modificateur de vignette peuvent inclure des variables définies par l’utilisateur.
seo-title: Variables personnalisées
solution: Experience Manager
title: Variables personnalisées
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Custom variables{#custom-variables}

La partie des requêtes et les chaînes vignette::Modifier peuvent inclure des variables définies par l’utilisateur.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Variable name. Peut se composer de n’importe quelle combinaison de caractères alphabétiques, de chiffres et de caractères sûrs, à l’exclusion de &#39;$&#39;.

** *[!DNL value]* ** Valeur à laquelle la variable doit être définie (chaîne).

Les variables sont définies de la même manière que les autres commandes du serveur, à l’aide de la syntaxe ci-dessus. Les variables doivent être définies avant d’être référencées. Les variables définies dans `vignette::Modifier` peuvent être référencées dans la requête d’URL, et inversement.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>*[!DNL value]* doit être codé en URL à un seul passage pour une transmission HTTP sécurisée. Le -codage est requis si *[!DNL value]* est retransmis via HTTP. C’est le cas lorsqu’ *[!DNL value]* il est remplacé par une requête étrangère imbriquée.

Les variables sont référencées en incorporant le nom de la variable (entre un $ de début et un $ de fin) n’importe où dans les valeurs de commande. Par exemple, entre le &quot;=&quot; qui suit le nom de la commande et le &quot;&amp;&quot; suivant ou la fin de la requête. Le serveur remplace chaque occurrence de $ *[!DNL name]*$ par *[!DNL string]*. Aucune substitution ne se produira sur les occurrences de $ *[!DNL name]*$ dans les noms de commande (avant le signe égal d’une commande) et dans la partie chemin de la requête.

Les variables personnalisées ne peuvent pas être imbriquées. Les occurrences de $ *[!DNL name]*$ dans *[!DNL string]* le fichier ne sont pas remplacées. Par exemple, le fragment de requête `$var2=apple&$var1=my$var2$tree&text=$var1$` se résout `text=my$var2$tree`.

$ n’est pas un caractère réservé ; il peut se produire autrement dans la requête. Par exemple, `src=my$texture$file.tif` est une commande valide (en supposant qu’une entrée de catalogue de matières ou un fichier de texture nommé [!DNL my$texture$file.tif] existe), mais `wid=$number$` ne l’est pas, car `wid=` requiert un argument numérique.
