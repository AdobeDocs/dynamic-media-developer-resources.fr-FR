---
title: Gestion des couleurs
description: La spécification RTF autorise les valeurs de couleur de RGB spécifiées avec &bsol;colortbl. Chaque composant est fourni séparément avec les commandes &bsol;rouge, &bsol;vert et &bsol;bleu.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Gestion des couleurs{#color-handling}

La spécification RTF autorise les valeurs de couleur RGB spécifiées avec `\colortbl`. Chaque composant est fourni séparément avec la fonction `\red`, `\green`, et `\blue` des commandes.

La commande d’extension RTF propriétaire `\cmykcolortbl` permet de spécifier les couleurs CMJN, chaque composant de couleur étant fourni avec la propriété `\cyan`, `\magenta`, `\yellow`, et `\black` des commandes.

Valeurs des composants de couleur pour `\colortbl` sont compris entre 0 et 255. Valeurs de composant pour `\cmykcolortbl` sont compris entre 0 et 100.

La commande d’extension RTF `\*\iscolortbl`, pris en charge par `textPs=`, permet de spécifier un tableau de couleurs avec des valeurs colorimétriques de diffusion d’images standard, avec prise en charge complète du RGB, du gris, du CMJN et de l’alpha. La syntaxe est la suivante :

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* une ou plusieurs valeurs de couleur IS, séparées par &quot;;&quot;

Plusieurs types de table colorimétrique peuvent être spécifiés dans le même `text=` ou `textPs=` Chaîne RTF. Chaque table de couleurs peut avoir un nombre d’entrées différent. La diffusion d’images tente de trouver les couleurs dans cet ordre : `\iscolortbl` before `\cmykcolortbl` (uniquement si le type de pixel du calque de texte est CMJN) avant `\colortbl`. Pour `textPs=` uniquement, les couleurs sont converties avec précision entre CMJN et RGB, si cela est nécessaire (par exemple, lorsque des couleurs RGB sont spécifiées, mais que la sortie CMJN est requise). Si aucune couleur n’est trouvée pour une valeur d’index particulière, la couleur par défaut (noir) est utilisée.

Voir [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) pour une description de la syntaxe des valeurs de couleur IS.

## Restrictions {#section-c5173e672d854e4aa9656844f7fc4d0e}

Le modificateur `text=` ne prend pas en charge `\*\iscolortbl`. Le modificateur `textPs=` ne prend pas en charge `\cmykcolortbl`.

Les sélections de couleurs sont ignorées lors du rendu des polices Photoshop.

## Exemple {#section-0f166bb72bd44479be01131077851142}

Permet de contrôler trois couleurs de texte avec des variables tout en affichant la valeur par défaut de la couleur lorsque la chaîne RTF est ouverte dans un éditeur de texte RTF standard.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
