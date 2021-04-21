---
description: Les macros de commande fournissent des raccourcis nommés pour les jeux de commandes.
solution: Experience Manager
title: Macros de commande *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 1%

---


# Macros de commande *{#command-macros}

Les macros de commande fournissent des raccourcis nommés pour les jeux de commandes.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Nom de la macro

Les macros sont définies dans des fichiers de définition de macro distincts, qui peuvent être joints à des catalogues de matériaux ou au catalogue par défaut.

*[!DNL name]* n&#39;est pas sensible à la casse et peut se composer de n&#39;importe quelle combinaison de lettres ASCII, de chiffres, de &#39;-&#39;, &#39;_&#39; et &#39;.&#39; caractères.

Appelez des macros n’importe où dans une requête après le &#39;?&#39; ou n’importe où dans un champ `vignette::Modifier`. Les macros ne peuvent représenter qu’une ou plusieurs commandes de rendu d’image complètes et doivent être séparées des autres commandes avec des séparateurs &quot;&amp;&quot;.

Les appels de macros sont remplacés par leurs chaînes de substitution au début de l’analyse. Les commandes des macros remplacent les mêmes commandes dans la requête si elles surviennent avant l’appel de macro dans la requête. Ceci est différent de `vignette::Modifier`, où les commandes de la chaîne de requête remplacent toujours les commandes de la chaîne `vignette::Modifier`, quelle que soit la position de la requête.

Les macros de commande ne peuvent pas avoir de valeurs d’argument, mais des variables personnalisées peuvent être utilisées pour transmettre des valeurs de la requête à la macro.

Il est possible que les macros ne soient pas imbriquées.

**Exemple**

Les macros peuvent s’avérer utiles si les mêmes commandes ou attributs doivent être appliqués à des images générées différentes.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Vous pouvez définir une macro pour les attributs communs :

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro serait utilisée comme suit :

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Comme `qlt=` est différent pour la troisième requête, nous remplaçons simplement la valeur après l’appel de la macro (en spécifiant `qlt=`*avant* `$render$`n’aurait aucun effet).

**Voir aussi**

`catalog::MacroFile`,  `catalog::Modifier`, Référence de la définition de macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

