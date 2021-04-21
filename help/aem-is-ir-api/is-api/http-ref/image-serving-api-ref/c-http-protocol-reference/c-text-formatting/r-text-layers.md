---
description: textPs= prend en charge plusieurs modèles d’utilisation différents décrits dans cette section.
solution: Experience Manager
title: calques de texte
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 0%

---


# Calques de texte{#text-layers}

textPs= prend en charge plusieurs modèles d’utilisation différents décrits dans cette section.

>[!NOTE]
>
>Cette section ne s&#39;applique pas à `text=`.

Les règles et définitions communes sont les suivantes :

* Les calques de texte de dimensionnement automatique sont des calques qui n’incluent pas de commande `size=` ou pour lesquels `size=0,0` est spécifié.

* La taille de calque des calques de texte à redimensionnement automatique est déterminée par le texte généré.
* En règle générale, l’ancre de calque par défaut des calques de texte à taille automatique est inférieure à *et non* au centre du calque (voir ci-dessous).
* Si `anchor=` ou `origin=` est spécifié pour les calques de texte à redimensionnement automatique, la position du calque de texte est influencée par le contenu du texte.

* Lorsque `size=` est spécifié, des parties de glyphes de caractères peuvent être rendues en dehors du rectangle du calque.
* `pos=` peut être utilisé dans tous les cas pour repositionner un calque de texte.

## Texte en points (auto-dimensionnement) {#section-db99ec98eb114458b2dbc9911a58f74a}

Le texte de point de style Photoshop est simulé lorsque `textPs=` est spécifié sans `size=`, `textPath=` ou `textFlowPath=`. La taille du calque est déterminée horizontalement par la largeur du texte rendu et verticalement par l’interligne. Le texte ne sera jamais automatiquement renvoyé à la ligne.

Si aucun élément `anchor=` ou `origin=` n&#39;est spécifié, la première ligne du texte est placée immédiatement au-dessus de l&#39;origine du calque ; les paragraphes marqués avec `\ql` sont positionnés à droite de l’origine de calque, les paragraphes qui incluent `\qr` sont rendus à gauche de l’origine et les paragraphes avec `\qc` sont centrés horizontalement autour de l’origine. Les règles standard de positionnement des calques s’appliquent si `anchor=` ou `origin=` sont spécifiées.

Si `color=` est spécifié, il remplit le cadre de sélection du texte affiché.

Les commandes RTF suivantes sont ignorées : `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Zone de texte rectangulaire {#section-1d3ab11df26d4004a1a801546756475d}

Si `size=` est spécifié en plus de `textPs=` (sans `textPath=` et `textFlowPath=`), le texte est limité au rectangle spécifié. Le calque est positionné comme d’habitude. Les glyphes de caractères près des bords de la zone de texte peuvent être rendus partiellement en dehors de la zone de texte.

`color=` remplit la région définie par  `size=`.

Toutes les commandes RTF sont appliquées comme prévu.

## Zone de texte de hauteur de variable {#section-e1233d1c9f8e43218667361dc0c4fd06}

Si vous spécifiez `size=` avec une hauteur de 0, la zone de texte peut être dimensionnée verticalement pour contenir tout le contenu. La largeur du calque est définie par la largeur de `size=` et la hauteur du calque par la hauteur du texte rendu réel. Le calque est positionné comme d’habitude. Les glyphes de caractères situés à proximité des bords gauche et droit de la zone de texte peuvent être rendus partiellement en dehors de la zone de texte.

`color=` remplit le rectangle défini par la largeur spécifiée  `size=` et la hauteur du texte affiché.

Les commandes RTF suivantes sont ignorées :

`\vertal*`

## Auto-dimensionnement du texte dans le chemin {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` en conjonction avec  `textPs=` peut être utilisé pour définir une ou plusieurs régions dans lesquelles le texte doit être enchaîné. `textFlowXPath=` peut être spécifié de manière facultative pour exclure le texte de l’entrée dans une ou plusieurs zones. Si `size=` n’est pas spécifié, le calque de texte résultant est auto-dimensionné et la taille du calque est déterminée par le cadre de sélection du texte effectivement rendu.

Si aucun élément `origin=` ou `anchor=` n’est spécifié, l’ancre de calque prend par défaut (0,0) l’espace de coordonnées de pixels utilisé pour définir le ou les chemins d’accès, assurant ainsi un positionnement absolu quel que soit le texte rendu. Si `anchor=` ou `origin=` sont spécifiés, le calque est positionné par rapport au cadre de sélection du contenu réel rendu (et s’y adapte).

`color=` remplit le cadre de sélection du texte affiché.

Les commandes RTF suivantes sont ignorées :

`\marg*`

## Texte prédimensionné dans le chemin {#section-ed492a8a54414cd4bde360500cec6968}

Si `size=` est spécifié avec `textFlowPath=`, la taille du calque est prédéterminée. (0,0) de l’espace de coordonnées de pixels utilisé pour définir le ou les chemins se trouve dans le coin supérieur gauche du rectangle de calque.

Les régions `textFlowPath=` peuvent se trouver en dehors du rectangle du calque. Le texte est toujours distribué et généré dans toutes les zones de chemin, même si le texte est rendu en dehors du rectangle du calque. `extend=0,0,0,0`peut être utilisé pour recadrer le texte rendu dans le rectangle du calque.

Pour le positionnement des calques, le rectangle de calque est basé sur le `size=` spécifié, quelle que soit la quantité de texte réellement rendu, même si une partie se trouve en dehors du rectangle de calque. Le positionnement standard des calques s’applique.

`color=` remplit la zone rectangulaire définie par  `size=`.

Les commandes RTF suivantes sont ignorées pour `textFlowPath=` :

`\marg*`

## Auto-dimensionnement du texte sur le chemin {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` définit un ou plusieurs chemins sur lesquels le texte spécifié  `textPs=` doit être rendu. Si `size=` n’est pas spécifié, le calque de texte résultant est auto-dimensionné. La taille du calque est déterminée par le cadre de sélection du texte affiché.

Si aucun élément `origin=` ou `anchor=` n’est spécifié, l’ancre de calque prend par défaut (0,0) l’espace de coordonnées de pixels utilisé pour définir le chemin d’accès ; la position du texte rendu est fixe, quelle que soit la quantité de texte généré. Si `anchor=` ou `origin=` sont spécifiés, le calque est positionné par rapport au cadre de sélection du contenu réel rendu (et s’y adapte).

`color=` remplit le cadre de sélection du texte affiché.

Les commandes RTF suivantes sont ignorées :

* `\marg*`
* `\hyph*`
* `\vertal*`

Tout texte situé après le premier `\par` ou `\line` est ignoré.

## Texte prédimensionné sur le chemin {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Si `size=` est spécifié avec `textPath=`, la taille du calque est prédéterminée. (0,0) de l’espace de coordonnées de pixels utilisé pour définir le ou les chemins se trouve dans le coin supérieur gauche du rectangle de calque.

Les chemins peuvent être situés partiellement ou entièrement à l’extérieur du rectangle du calque. Le texte est toujours appliqué et rendu le long du chemin entier, même en dehors du rectangle du calque. `extend=0,0,0,0` peut être utilisé pour recadrer le texte rendu dans le rectangle du calque.

Pour le positionnement des calques, le rectangle du calque est basé sur le `size=` spécifié, même si une partie du texte est rendue en dehors du rectangle du calque. Le positionnement standard des calques s’applique.

`color=` remplit la zone définie par  `size=`.

Les commandes RTF suivantes sont ignorées :

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Tout texte situé après le premier `\par` ou `\line` est ignoré.
