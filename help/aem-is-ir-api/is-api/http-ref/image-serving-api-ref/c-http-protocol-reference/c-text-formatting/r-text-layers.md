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
>Cette section ne s&#39;applique pas à `text=`.

Les règles et définitions courantes sont les suivantes :

* Les calques de texte auto-dimensionnés sont des calques qui n’incluent pas de commande `size=` ou pour lesquels `size=0,0` est spécifié.

* La taille du calque des calques de texte de redimensionnement automatique est déterminée par le texte généré.
* L’ancre de calque par défaut des calques de texte de redimensionnement automatique est généralement de *et non* au centre du calque (voir ci-dessous).
* Si `anchor=` ou `origin=` est spécifié pour les calques de texte auto-dimensionnés, la position du calque de texte est influencée par le contenu du texte.

* Lorsque `size=` est spécifié, des parties de glyphes de caractères peuvent être rendues en dehors du rectangle du calque.
* `pos=` peut être utilisé dans tous les cas pour repositionner une couche de texte.

## Texte du point (auto-dimensionnement) {#section-db99ec98eb114458b2dbc9911a58f74a}

Le texte de point de style Photoshop est simulé lorsque `textPs=` est spécifié sans `size=`, `textPath=` ou `textFlowPath=`. La taille du calque est déterminée horizontalement par la largeur du texte rendu et verticalement par l’interligne. Le texte n’est jamais automatiquement renvoyé à la ligne.

Si aucun paramètre `anchor=` ou `origin=` n’est spécifié, la première ligne du texte est positionnée immédiatement au-dessus de l’origine du calque ; les paragraphes marqués de `\ql` sont positionnés à droite de l’origine du calque, les paragraphes qui incluent `\qr` sont rendus à gauche de l’origine et les paragraphes avec `\qc` sont centrés horizontalement autour de l’origine. Les règles de positionnement des calques standard s’appliquent si `anchor=` ou `origin=` sont spécifiées.

Si `color=` est spécifié, il remplit le cadre de sélection du texte affiché.

Les commandes RTF suivantes sont ignorées : `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Zone de texte rectangulaire {#section-1d3ab11df26d4004a1a801546756475d}

Si `size=` est spécifié en plus de `textPs=` (sans `textPath=` et `textFlowPath=`), le texte est limité au rectangle spécifié. Le calque est positionné comme vous le faites habituellement. Les glyphes de caractères près des bords de la zone de texte peuvent être rendus partiellement en dehors de la zone de texte.

`color=` remplit la région définie par `size=`.

Toutes les commandes RTF sont appliquées comme prévu.

## Zone de texte Hauteur variable {#section-e1233d1c9f8e43218667361dc0c4fd06}

La spécification de `size=` avec une hauteur de 0 permet de dimensionner la zone de texte verticalement pour l’adapter à tous les contenus. La largeur du calque est définie par la largeur de `size=` et la hauteur du calque par la hauteur du texte rendu réel. Le calque est positionné comme vous le faites habituellement. Les glyphes de caractères près des bords gauche et droit de la zone de texte peuvent être rendus partiellement en dehors de la zone de texte.

`color=` remplit le rectangle défini par la largeur spécifiée avec `size=` et la hauteur du texte affiché.

Les commandes RTF suivantes sont ignorées :

`\vertal*`

## Auto-dimensionnement du texte dans le chemin {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` peut être utilisé conjointement avec `textPs=` pour définir une ou plusieurs régions dans lesquelles le texte doit être enchaîné. `textFlowXPath=` peut être spécifié de manière facultative pour exclure le texte de l’entrée dans une ou plusieurs zones. Si `size=` n’est pas spécifié, le calque de texte obtenu est auto-dimensionné et la taille du calque est déterminée par le cadre de sélection du texte réellement rendu.

Si aucun `origin=` ou `anchor=` n’est spécifié, l’ancre de calque correspond par défaut à (0,0) de l’espace de coordonnées de pixel utilisé pour définir le ou les chemins d’accès, en veillant au positionnement absolu, quel que soit le texte rendu. Si `anchor=` ou `origin=` sont spécifiés, le calque est positionné par rapport au cadre de sélection (et en l’adaptant) du contenu réel rendu.

`color=` remplit le cadre de sélection du texte affiché.

Les commandes RTF suivantes sont ignorées :

`\marg*`

## Texte prédimensionné dans le chemin {#section-ed492a8a54414cd4bde360500cec6968}

Si `size=` est spécifié avec `textFlowPath=`, la taille du calque est prédéterminée. (0,0) de l’espace de coordonnées en pixels utilisé pour définir le ou les chemins d’accès se trouve dans le coin supérieur gauche du rectangle du calque.

Les régions `textFlowPath=` peuvent se trouver en dehors du rectangle du calque. Le texte est toujours mis en page et rendu dans toutes les zones du chemin, même si cela entraîne le rendu du texte en dehors du rectangle du calque. `extend=0,0,0,0` peut être utilisé pour recadrer le texte rendu dans le rectangle du calque.

À des fins de positionnement des calques, le rectangle du calque est basé sur le `size=` spécifié, quelle que soit la quantité de texte réellement restituée, même si une partie se trouve en dehors du rectangle du calque. Le positionnement des calques standard s’applique.

`color=` remplit la zone rectangulaire définie par `size=`.

Les commandes RTF suivantes sont ignorées pour `textFlowPath=` :

`\marg*`

## Auto-dimensionnement du texte sur le chemin {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` définit un ou plusieurs chemins sur lesquels le texte spécifié avec `textPs=` doit être rendu. Lorsque `size=` n’est pas spécifié, le calque de texte obtenu est auto-dimensionné. La taille du calque est déterminée par le cadre de sélection du texte affiché.

Si aucune valeur `origin=` ou `anchor=` n’est spécifiée, l’ancre de calque correspond par défaut à (0,0) l’espace de coordonnées de pixel utilisé pour définir le chemin ; la position du texte rendu est fixe, quelle que soit la quantité de texte rendue. Si `anchor=` ou `origin=` sont spécifiés, le calque est positionné par rapport au cadre de sélection (et en l’adaptant) du contenu réel rendu.

`color=` remplit le cadre de sélection du texte affiché.

Les commandes RTF suivantes sont ignorées :

* `\marg*`
* `\hyph*`
* `\vertal*`

Tout texte après le premier `\par` ou `\line` est ignoré.

## Texte prédimensionné sur le chemin {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Si `size=` est spécifié avec `textPath=`, la taille du calque est prédéterminée. (0,0) de l’espace de coordonnées en pixels utilisé pour définir le ou les chemins d’accès se trouve dans le coin supérieur gauche du rectangle du calque.

Les chemins peuvent être situés partiellement ou entièrement en dehors du rectangle du calque. Le texte est toujours appliqué et rendu sur l’ensemble du chemin, même en dehors du rectangle du calque. `extend=0,0,0,0` peut être utilisé pour recadrer le texte rendu dans le rectangle du calque.

Pour le positionnement des calques, le rectangle du calque est basé sur le `size=` spécifié, même si une partie du texte est rendue en dehors du rectangle du calque. Le positionnement des calques standard s’applique.

`color=` remplit la zone définie par `size=`.

Les commandes RTF suivantes sont ignorées :

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Tout texte après le premier `\par` ou `\line` est ignoré.
