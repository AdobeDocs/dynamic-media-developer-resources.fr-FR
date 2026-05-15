---
title: Gestion des couleurs
description: La spécification RTF autorise les valeurs de couleur RGB spécifiées avec &bsol;colortbl. Chaque composant est fourni séparément avec les commandes &bsol;red, &bsol;green et &bsol;blue.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
TQID: 'https://experienceleague.adobe.com/w5IfFwmdMegueJbDMjwvb5XCPuemRcJ1XTqcJFgdEMQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# Gestion des couleurs{#color-handling}

La spécification RTF autorise les valeurs de couleur RGB spécifiées avec `\colortbl`. Chaque composant est fourni séparément avec les commandes `\red`, `\green` et `\blue`.

La `\cmykcolortbl` de commande d’extension RTF propriétaire permet de spécifier des couleurs CMJN, chaque composant de couleur étant fourni avec les commandes `\cyan`, `\magenta`, `\yellow` et `\black`.

Les valeurs des composants de couleur pour `\colortbl` sont comprises entre 0 et 255. Les valeurs des composants pour `\cmykcolortbl` sont comprises entre 0 et 100.

La `\*\iscolortbl` de commande d’extension RTF, prise en charge par `textPs=`, permet de spécifier une table des couleurs avec des valeurs de couleur de diffusion d’image standard, avec une prise en charge complète de RGB, du gris, de CMJN et de la version alpha. Elle présente la syntaxe suivante :

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* une ou plusieurs valeurs de couleur IS, séparées par des ’;’

Plusieurs types de tableaux de couleurs peuvent être spécifiés dans la même chaîne RTF `text=` ou `textPs=`. Chaque tableau des couleurs peut avoir un nombre d’entrées différent. La diffusion d’images tente de trouver des couleurs dans cet ordre : `\iscolortbl` avant `\cmykcolortbl` (uniquement si le type de pixel du calque de texte est CMJN) avant `\colortbl`. Pour `textPs=` uniquement, les couleurs sont converties avec précision entre CMJN et RGB, si nécessaire (par exemple, lorsque des couleurs RGB sont spécifiées mais qu’une sortie CMJN est requise). Si aucune couleur n’est trouvée pour une valeur d’index particulière, la couleur par défaut (noir) est utilisée.

Reportez-vous à [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) pour une description de la syntaxe des valeurs de couleur IS.

## Restrictions {#section-c5173e672d854e4aa9656844f7fc4d0e}

Le modificateur `text=` ne prend pas en charge `\*\iscolortbl`. Le modificateur `textPs=` ne prend pas en charge `\cmykcolortbl`.

Les sélections de couleurs sont ignorées lors du rendu de Photofonts.

## Exemple {#section-0f166bb72bd44479be01131077851142}

Permet de contrôler trois couleurs de texte avec des variables, tout en affichant la valeur par défaut de la couleur lorsque la chaîne RTF est ouverte dans un éditeur de texte RTF standard.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
