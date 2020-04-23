---
description: La spécification RTF autorise les valeurs de couleur RVB spécifiées avec \colortbl. Chaque composant est fourni séparément avec les commandes \red, \green et \blue.
seo-description: La spécification RTF autorise les valeurs de couleur RVB spécifiées avec \colortbl. Chaque composant est fourni séparément avec les commandes \red, \green et \blue.
seo-title: Gestion des couleurs
solution: Experience Manager
title: Gestion des couleurs
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 341693d69fc414dacf984d66e2eaeba2418e663b

---


# Gestion des couleurs{#color-handling}

La spécification RTF autorise les valeurs de couleur RVB spécifiées avec `\colortbl`. Chaque composant est fourni séparément avec les commandes `\red`, `\green`et `\blue` .

La commande d’extension RTF propriétaire `\cmykcolortbl` permet de spécifier les couleurs CMJN, chaque composante de couleur étant fournie avec les commandes `\cyan`, `\magenta`, `\yellow`et `\black` .

Les valeurs des composants de couleur pour `\colortbl` sont comprises entre 0 et 255. Les valeurs de composant pour `\cmykcolortbl` sont comprises entre 0 et 100.

La commande d’extension RTF `\*\iscolortbl`, prise en charge par `textPs=`, permet de spécifier une table de couleurs avec des valeurs de couleur standard pour la diffusion d’images, avec prise en charge RVB, gris, CMJN et alpha complète. Il a la syntaxe suivante :

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* une ou plusieurs valeurs de couleur IS, séparées par &#39;;&#39;

Plusieurs types de table de couleurs peuvent être spécifiés dans la même chaîne `text=` ou `textPs=` RTF. Chaque table de couleurs peut comporter un nombre d’entrées différent. La diffusion d’images tente de trouver les couleurs dans cet ordre : `\iscolortbl` avant `\cmykcolortbl` (uniquement si le type de pixel du calque de texte est CMJN) avant `\colortbl`. Pour `textPs=` seulement, les couleurs sont converties avec précision entre CMJN et RVB, le cas échéant (par exemple, lorsque des couleurs RVB sont spécifiées mais que la sortie CMJN est requise). Si aucune couleur n’est trouvée pour une valeur d’index particulière, la couleur par défaut (noir) est utilisée.

Reportez-vous à [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) pour obtenir une description de la syntaxe des valeurs de couleur IS.

## Restrictions {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` ne prend pas en charge `\*\iscolortbl`. `textPs=` ne prend pas en charge `\cmykcolortbl`.

Les sélections de couleurs sont ignorées lors du rendu des polices Photoshop.

## Exemple {#section-0f166bb72bd44479be01131077851142}

Permet de contrôler trois couleurs de texte avec des variables, tout en affichant la valeur par défaut de la couleur lorsque la chaîne RTF est ouverte dans un éditeur de texte RTF standard.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
