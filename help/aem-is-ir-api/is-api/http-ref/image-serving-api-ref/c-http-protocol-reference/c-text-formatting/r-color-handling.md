---
title: Gestion des couleurs
description: La spécification RTF autorise les valeurs de couleur de RGB spécifiées avec &bsol;colortbl. Chaque composant est fourni séparément avec les commandes &bsol;rouge, &bsol;vert et &bsol;bleu.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Gestion des couleurs{#color-handling}

La spécification RTF autorise les valeurs de couleur de RGB spécifiées avec `\colortbl`. Chaque composant est fourni séparément avec les commandes `\red`, `\green` et `\blue`.

La commande d’extension RTF propriétaire `\cmykcolortbl` permet de spécifier des couleurs CMJN, chaque composant de couleur étant fourni avec les commandes `\cyan`, `\magenta`, `\yellow` et `\black`.

Les valeurs des composants de couleur pour `\colortbl` sont comprises entre 0 et 255. Les valeurs des composants pour `\cmykcolortbl` sont comprises entre 0 et 100.

La commande d’extension RTF `\*\iscolortbl`, prise en charge par `textPs=`, permet de spécifier une table de couleurs avec des valeurs de couleur standard du serveur d’images, avec prise en charge complète du RGB, du gris, du CMJN et de l’alpha. La syntaxe est la suivante :

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* une ou plusieurs valeurs de couleur IS, séparées par &quot;;&quot;

Plusieurs types de table colorimétrique peuvent être spécifiés dans la même chaîne RTF `text=` ou `textPs=`. Chaque table de couleurs peut avoir un nombre d’entrées différent. La diffusion d’image tente de trouver les couleurs dans cet ordre : `\iscolortbl` avant `\cmykcolortbl` (uniquement si le type de pixel de la couche de texte est CMJN) avant `\colortbl`. Pour `textPs=` uniquement, les couleurs sont converties avec précision entre CMJN et RGB, si cela est nécessaire (par exemple, lorsque des couleurs de RGB sont spécifiées, mais que la sortie CMJN est requise). Si aucune couleur n’est trouvée pour une valeur d’index particulière, la couleur par défaut (noir) est utilisée.

Reportez-vous à [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) pour une description de la syntaxe des valeurs de couleur IS.

## Restrictions {#section-c5173e672d854e4aa9656844f7fc4d0e}

Le modificateur `text=` ne prend pas en charge `\*\iscolortbl`. Le modificateur `textPs=` ne prend pas en charge `\cmykcolortbl`.

Les sélections de couleurs sont ignorées lors du rendu des polices Photoshop.

## Exemple {#section-0f166bb72bd44479be01131077851142}

Permet de contrôler trois couleurs de texte avec des variables tout en affichant la valeur par défaut de la couleur lorsque la chaîne RTF est ouverte dans un éditeur de texte RTF standard.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
