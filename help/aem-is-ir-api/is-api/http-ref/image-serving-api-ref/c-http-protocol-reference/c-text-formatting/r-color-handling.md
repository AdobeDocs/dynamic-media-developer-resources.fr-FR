---
description: La spécification RTF autorise les valeurs de couleur RVB spécifiées avec &bsol;colortbl. Chaque composant est fourni séparément avec les commandes &bsol;rouge, &bsol;vert et &bsol;bleu.
solution: Experience Manager
title: Gestion des couleurs
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Gestion des couleurs{#color-handling}

La spécification RTF autorise les valeurs de couleur RVB spécifiées avec `\colortbl`. Chaque composant est fourni séparément avec les commandes `\red`, `\green` et `\blue`.

La commande d’extension RTF propriétaire `\cmykcolortbl` permet de spécifier des couleurs CMJN, chaque composant de couleur étant fourni avec les commandes `\cyan`, `\magenta`, `\yellow` et `\black`.

Les valeurs des composants de couleur pour `\colortbl` sont comprises entre 0 et 255. Les valeurs des composants pour `\cmykcolortbl` se situent dans la plage 0 à 100.

La commande d’extension RTF `\*\iscolortbl`, prise en charge par `textPs=`, permet de spécifier un tableau de couleurs avec des valeurs de couleur standard de diffusion d’images, avec prise en charge complète de RVB, de gris, de CMJN et d’alpha. La syntaxe est la suivante :

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* une ou plusieurs valeurs de couleur IS, séparées par &quot;;&quot;

Plusieurs types de table colorimétrique peuvent être spécifiés dans la même chaîne `text=` ou `textPs=` RTF. Chaque table de couleurs peut avoir un nombre d’entrées différent. La diffusion d’images tente de trouver les couleurs dans cet ordre : `\iscolortbl` devant `\cmykcolortbl` (uniquement si le type de pixel de la couche de texte est CMJN) avant `\colortbl`. Pour `textPs=` uniquement, les couleurs sont converties avec précision entre CMJN et RVB, si cela est nécessaire (par exemple, lorsque les couleurs RVB sont spécifiées, mais que la sortie CMJN est requise). Si aucune couleur n’est trouvée pour une valeur d’index particulière, la couleur par défaut (noir) est utilisée.

Reportez-vous à [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) pour une description de la syntaxe des valeurs de couleur IS.

## Restrictions {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` ne prend pas en charge  `\*\iscolortbl`. `textPs=` ne prend pas en charge  `\cmykcolortbl`.

Les sélections de couleurs sont ignorées lors du rendu des polices Photoshop.

## Exemple {#section-0f166bb72bd44479be01131077851142}

Permet de contrôler trois couleurs de texte avec des variables tout en affichant la valeur par défaut de la couleur lorsque la chaîne RTF est ouverte dans un éditeur de texte RTF standard.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
