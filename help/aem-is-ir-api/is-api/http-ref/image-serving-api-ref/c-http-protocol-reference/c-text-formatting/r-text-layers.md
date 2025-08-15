---
description: textPs= prend en charge un certain nombre de modèles d’utilisation différents décrits dans cette section.
solution: Experience Manager
title: Calques de texte
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# Calques de texte{#text-layers}

textPs= prend en charge un certain nombre de modèles d’utilisation différents décrits dans cette section.

>[!NOTE]
>
>Cette section ne s’applique pas à `text=`.

Les règles et définitions courantes sont les suivantes :

* Les calques de texte auto-dimensionnants sont des calques qui n’incluent pas de commande ou pour lesquels `size=` est `size=0,0` spécifiée.

* La taille de calque des calques de texte autodimensionnés est déterminée par le texte réel rendu.
* L’ancre de calque par défaut des calques de texte auto-dimensionnés n’est généralement *pas* au centre du calque (voir ci-dessous).
* Si `anchor=` ou `origin=` est spécifié pour les calques de texte auto-dimensionnés, la position du calque de texte est influencée par le contenu du texte.

* Lorsque `size=` est spécifié, des parties de glyphes de caractères peuvent être rendues en dehors du rectangle de calque.
* `pos=` peut être utilisé dans tous les cas pour repositionner un calque de texte.

## Texte ponctuel (auto-dimensionnement) {#section-db99ec98eb114458b2dbc9911a58f74a}

Le texte de point Photoshop style est simulé lorsque `textPs=` est spécifié sans `size=`, `textPath=`, ou `textFlowPath=`. La taille du calque est déterminée horizontalement par la largeur du texte rendu et verticalement par l’interligne. Le texte n’est jamais renvoyé automatiquement à la ligne.

Si ni l’un `anchor=` ni l’autre ne `origin=` sont spécifiés, la première ligne du texte est placée immédiatement au-dessus de l’origine du calque ; les paragraphes marqués par `\ql` sont positionnés à droite de l’origine du calque, les paragraphes qui incluent `\qr` sont rendus à gauche de l’origine et les paragraphes avec `\qc` sont centrés horizontalement autour de l’origine. Les règles standard de positionnement de calque s’appliquent si `anchor=` elles `origin=` sont spécifiées.

Si `color=` est spécifié, il remplit le cadre de sélection du texte réellement rendu.

Les commandes RTF suivantes sont ignorées : `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Zone de texte rectangulaire {#section-1d3ab11df26d4004a1a801546756475d}

Si `size=` est spécifié en plus de `textPs=` (sans `textPath=` et `textFlowPath=`), le texte est limité au rectangle spécifié. Le calque est positionné comme d’habitude. Les glyphes de caractères situés près des bords de la zone de texte peuvent être rendus partiellement en dehors de la zone de texte.

`color=` Remplit la région définie par `size=`.

Toutes les commandes RTF sont appliquées comme prévu.

## Zone de texte à hauteur variable {#section-e1233d1c9f8e43218667361dc0c4fd06}

Si vous spécifiez `size=` une hauteur 0, la zone de texte peut être dimensionnée verticalement pour s’adapter à tous les contenus. La largeur du calque est définie par la largeur de `size=`, et la hauteur du calque par la hauteur du texte réellement rendu. Le calque est positionné comme d’habitude. Les glyphes de caractères situés près des bords gauche et droit de la zone de texte peuvent être rendus partiellement en dehors de la zone de texte.

`color=` Remplit le rectangle défini par la largeur spécifiée avec `size=` et la hauteur du texte réel rendu.

Les commandes RTF suivantes sont ignorées :

`\vertal*`

## Texte autodimensionné dans le chemin d’accès {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` en conjonction avec `textPs=` peut être utilisé pour définir une ou plusieurs régions dans lesquelles le texte doit être enchaîné. `textFlowXPath=` peut être spécifié de manière facultative pour empêcher le texte de circuler dans une ou plusieurs zones. Si `size=` n’est pas spécifié, le calque de texte résultant est auto-dimensionné et la taille du calque est déterminée par le cadre de sélection du texte réellement rendu.

Si ni l’un `origin=` ni l’autre n’est `anchor=` spécifié, l’ancre de calque prend par défaut la valeur (0,0) de l’espace de coordonnées en pixels utilisé pour définir le(s) chemin(s), garantissant un positionnement absolu quel que soit le texte rendu. Si `anchor=` ou `origin=` sont spécifiés, le calque est positionné par rapport (et s’adaptant à) le cadre de sélection du contenu réel rendu.

`color=` Remplit le cadre de sélection du texte réellement rendu.

Les commandes RTF suivantes sont ignorées :

`\marg*`

## Texte prédimensionné dans le chemin d’accès {#section-ed492a8a54414cd4bde360500cec6968}

Si `size=` est spécifié avec `textFlowPath=`, la taille du calque est prédéterminée. (0,0) de l’espace de coordonnées des pixels utilisé pour définir le(s) chemin(s) est situé dans le coin supérieur gauche du rectangle calque.

Les `textFlowPath=` régions peuvent être situées à l’extérieur du rectangle du calque. Le texte est toujours enchaîné et rendu dans toutes les régions de chemin, même si cela entraîne le rendu du texte en dehors du rectangle du calque. `extend=0,0,0,0`peut être utilisée pour recadrer le texte généré dans le rectangle du calque.

À des fins de positionnement de calque, le rectangle de calque est basé sur le , quelle que soit la `size=`quantité de texte réellement rendue, même si une partie de celui-ci est située à l’extérieur du rectangle de calque. Le positionnement standard du calque s’applique.

`color=` Remplit la zone rectangulaire définie par `size=`.

Les commandes RTF suivantes sont ignorées pour `textFlowPath=`:

`\marg*`

## Texte auto-redimensionné sur le chemin d’accès {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` Définit un ou plusieurs chemins d’accès sur lesquels le texte indiqué dans `textPs=` doit être rendu. Si `size=` n’est pas spécifié, le calque de texte résultant se dimensionne automatiquement. La taille du calque est déterminée par le cadre de sélection du texte réellement rendu.

Si ni l’un `origin=` ni l’autre n’est `anchor=` spécifié, l’ancre de calque prend par défaut la valeur (0,0) de l’espace de coordonnées des pixels utilisé pour définir le tracé ; la position du texte rendu est fixe quelle que soit la quantité de texte rendue. Si `anchor=` ou `origin=` sont spécifiés, le calque est positionné par rapport (et s’adaptant à) le cadre de sélection du contenu réel rendu.

`color=` Remplit le cadre de sélection du texte réellement rendu.

Les commandes RTF suivantes sont ignorées :

* `\marg*`
* `\hyph*`
* `\vertal*`

Tout texte après le premier `\par` ou `\line` est ignoré.

## Texte prédimensionné sur le chemin {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Si `size=` est spécifié avec `textPath=`, la taille du calque est prédéterminée. (0,0) de l’espace de coordonnées des pixels utilisé pour définir le(s) chemin(s) est situé dans le coin supérieur gauche du rectangle calque.

Les tracés peuvent être situés partiellement ou entièrement à l’extérieur du rectangle calque. Le texte est toujours appliqué et rendu sur l’ensemble du tracé, même s’il se trouve en dehors du rectangle du calque. `extend=0,0,0,0` peut être utilisée pour recadrer le texte généré dans le rectangle du calque.

À des fins de positionnement de calque, le rectangle de calque est basé sur le , `size=`même si une partie du texte est rendue en dehors du rectangle de calque. Le positionnement standard du calque s’applique.

`color=` Remplit la zone définie par `size=`.

Les commandes RTF suivantes sont ignorées :

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Tout texte après le premier `\par` ou `\line` est ignoré.
