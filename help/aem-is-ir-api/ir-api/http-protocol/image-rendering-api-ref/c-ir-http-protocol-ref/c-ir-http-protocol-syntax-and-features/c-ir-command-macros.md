---
description: Les macros de commande fournissent des raccourcis nommés pour les ensembles de commandes.
seo-description: Les macros de commande fournissent des raccourcis nommés pour les ensembles de commandes.
seo-title: Macros de commande *
solution: Experience Manager
title: Macros de commande *
topic: Scene7 Image Serving - Image Rendering API
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Macros de commande *{#command-macros}

Les macros de commande fournissent des raccourcis nommés pour les ensembles de commandes.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Nom de la macro

Les macros sont définies dans des fichiers de définition de macro distincts, qui peuvent être joints à des catalogues de matières ou au catalogue par défaut.

*[!DNL name]* n’est pas sensible à la casse et peut se composer de n’importe quelle combinaison de lettres ASCII, de nombres, de &quot;-&quot;, de &quot;_&quot; et de &quot;.&quot; caractères.

Appelez des macros n’importe où dans une requête après le signe ? ou n’importe où dans un `vignette::Modifier` champ. Les macros ne peuvent représenter qu’une ou plusieurs commandes de rendu d’image complètes et doivent être séparées des autres commandes avec des séparateurs &quot;&amp;&quot;.

Les appels de macro sont remplacés par leurs chaînes de substitution tôt au cours de l’analyse. Les commandes des macros remplacent les mêmes commandes dans la requête si elles surviennent avant l’appel de macro dans la requête. Cela diffère de `vignette::Modifier`, où les commandes de la chaîne de requête remplacent toujours les commandes de la `vignette::Modifier` chaîne, quelle que soit la position dans la requête.

Les macros de commande ne peuvent pas avoir de valeurs d’argument, mais des variables personnalisées peuvent être utilisées pour transmettre des valeurs de la requête dans la macro.

Les macros ne peuvent pas être imbriquées.

**Exemple**

Les macros peuvent s’avérer utiles si les mêmes commandes ou attributs doivent être appliqués à des images de rendu différentes.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Vous pouvez définir une macro pour les attributs communs :

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro serait utilisée comme suit :

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Etant donné que `qlt=` est différent pour la troisième requête, nous remplaçons simplement la valeur après l’appel de la macro (la spécification `qlt=`*avant *n’`$render$`aurait aucun effet).

**Voir aussi**

`catalog::MacroFile`, `catalog::Modifier`Référence des définitions de macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

