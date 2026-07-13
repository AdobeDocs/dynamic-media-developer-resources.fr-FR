---
title: Macros de commande
description: Les macros de commande fournissent des raccourcis nommés pour des ensembles de commandes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
TQID: 'https://experienceleague.adobe.com/cXLJJQ5CS-Apmq-8qYV-ew-lcvfRjoNfIbl2qyyKB6U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Macros de commande{#command-macros}

Les macros de commande fournissent des raccourcis nommés pour des ensembles de commandes.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Nom de la macro

Les macros sont définies dans des fichiers de définition de macro distincts, qui peuvent être joints aux catalogues de matières ou au catalogue par défaut.

*[!DNL name]* n’est pas sensible à la casse et peut consister en toute combinaison de lettres ASCII, de chiffres , de caractères ’-’, ’_’ et ’.’.

Appelez des macros n’importe où dans une requête après le caractère « ? » ou n’importe où dans un champ `vignette::Modifier`. Les macros ne peuvent représenter qu&#39;une ou plusieurs commandes de rendu d&#39;image et doivent être séparées des autres commandes par des séparateurs &#39;&amp;&#39;.

Les appels de macro sont remplacés par leurs chaînes de substitution plus tôt pendant l’analyse. Les commandes contenues dans les macros remplacent les mêmes commandes dans la requête si elles se produisent avant l’appel de la macro dans la requête. Ce workflow est différent de `vignette::Modifier`, où les commandes de la chaîne de requête remplacent celles de la chaîne de `vignette::Modifier`, quelle que soit la position dans la requête.

Les macros de commande ne peuvent pas avoir de valeurs d’argument, mais des variables personnalisées peuvent être utilisées pour transmettre des valeurs de la requête dans la macro.

Les macros ne peuvent pas être imbriquées.

**Exemple**

Les macros peuvent s’avérer utiles si les mêmes commandes ou attributs doivent être appliqués à différents rendus d’image.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Vous pouvez définir une macro pour les attributs communs :

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro serait utilisée comme suit :

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Comme `qlt=` est différent pour la troisième requête, le logiciel remplace la valeur après l’appel de la macro (la spécification de `qlt=` *avant* `$render$` est inefficace).

**Voir aussi**

`catalog::MacroFile`, `catalog::Modifier`, Référence de définition de macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

