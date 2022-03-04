---
title: Macros de commande
description: Les macros de commande fournissent des raccourcis nommés pour les jeux de commandes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# Macros de commande{#command-macros}

Les macros de commande fournissent des raccourcis nommés pour les jeux de commandes.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Nom de la macro

Les macros sont définies dans des fichiers de définition de macro distincts, qui peuvent être joints à des catalogues de matériaux ou au catalogue par défaut.

*[!DNL name]* n’est pas sensible à la casse et peut se composer de n’importe quelle combinaison de lettres ASCII, de nombres, de &quot;-&quot;, de &quot;_&quot; et de &quot;.&quot; caractères.

Appeler des macros n’importe où dans une requête après &quot;?&quot; ou n’importe où dans une `vignette::Modifier` champ . Les macros ne peuvent représenter qu’une ou plusieurs commandes de rendu d’image et doivent être séparées des autres commandes avec les séparateurs &quot;&amp;&quot;.

Les appels de macro sont remplacés par leurs chaînes de substitution tôt lors de l’analyse. Les commandes des macros remplacent les mêmes commandes de la requête si elles se produisent avant l’appel de macro dans la requête. Ce workflow diffère de `vignette::Modifier`, où les commandes de la chaîne de requête remplacent les commandes dans la variable `vignette::Modifier` chaîne, quelle que soit la position dans la requête.

Les macros de commande ne peuvent pas comporter de valeurs d’argument, mais des variables personnalisées peuvent être utilisées pour transmettre des valeurs de la requête dans la macro.

Les macros ne peuvent pas être imbriquées.

**Exemple**

Les macros peuvent s’avérer utiles si les mêmes commandes ou attributs doivent être appliqués à différentes images générées.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Vous pouvez définir une macro pour les attributs communs :

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro sera utilisée comme suit :

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Parce que `qlt=` est différent pour la troisième requête, le logiciel remplace la valeur après l’appel de la macro (en spécifiant `qlt=` *before* `$render$`est inefficace).

**Voir aussi**

`catalog::MacroFile`, `catalog::Modifier`, Référence de définition de macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
