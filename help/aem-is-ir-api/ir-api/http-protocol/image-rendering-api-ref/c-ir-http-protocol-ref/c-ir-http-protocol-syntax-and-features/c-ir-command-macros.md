---
title: Macros de commande
description: Les macros de commandes fournissent des raccourcis nommés pour des ensembles de commandes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Macros de commande{#command-macros}

Les macros de commandes fournissent des raccourcis nommés pour des ensembles de commandes.

`$ *[!DNL name]*$`

**&#x200B; *[!DNL name]* &#x200B;** Nom de la macro

Les macros sont définies dans des fichiers de définition de macros distincts, qui peuvent être joints à des catalogues de matériaux ou au catalogue par défaut.

*[!DNL name]* n’est pas sensible à la casse et peut être constitué de n’importe quelle combinaison de lettres ASCII, de chiffres, de &#39;-&#39;, &#39;_&#39; et de &#39;.&#39; caractères.

Invoquez les macros n’importe où dans une requête après le « ? », ou n’importe où dans un `vignette::Modifier` champ. Les macros ne peuvent représenter qu’une ou plusieurs commandes Image Rendering et doivent être séparées des autres commandes avec des séparateurs &#39;&amp;&#39;.

Les appels de macro sont remplacés par leurs chaînes de substitution au début de l’analyse. Les commandes dans les macros remplacent les mêmes commandes dans la demande si elles se produisent avant l’appel de macro dans la demande. Ce processus est différent de `vignette::Modifier`, où les commandes de la chaîne de requête remplacent les commandes de la `vignette::Modifier` chaîne, quelle que soit la position dans la demande.

Les macros de commande ne peuvent pas avoir de valeurs d’argument, mais des variables personnalisées peuvent être utilisées pour transmettre des valeurs de la demande dans la macro.

Les macros ne peuvent pas être imbriquées.

**Exemple**

Les macros peuvent être utiles si les mêmes commandes ou attributs doivent être appliqués à différentes images rendues.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Vous pouvez définir une macro pour les attributs communs :

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

L’utilisation de la macro se présente comme suit :

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Comme `qlt=` est différent pour la troisième requête, le logiciel remplace la valeur après l’appel de la macro (spécifier `qlt=` *avant* `$render$`est inefficace).

**Voir aussi**

`catalog::MacroFile`, , `catalog::Modifier`Référence de définition de macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
