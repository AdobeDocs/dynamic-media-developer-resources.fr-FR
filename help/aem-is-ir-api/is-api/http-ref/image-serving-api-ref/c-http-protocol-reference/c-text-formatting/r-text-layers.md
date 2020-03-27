---
description: textPs= prend en charge plusieurs modèles d’utilisation décrits dans cette section.
seo-description: textPs= prend en charge plusieurs modèles d’utilisation décrits dans cette section.
seo-title: Calques de texte
solution: Experience Manager
title: Calques de texte
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ccef969-7c54-49ce-b6ff-ae4eabfcf99b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Calques de texte{#text-layers}

textPs= prend en charge plusieurs modèles d’utilisation décrits dans cette section.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Le présent article ne s&#39;applique pas à `text=`la.

Les règles et définitions communes sont les suivantes :

* Les calques de texte à redimensionnement automatique sont des calques qui n’incluent pas de `size=` commande ou pour lesquels `size=0,0` est spécifié.

* La taille du calque des calques de texte à redimensionnement automatique est déterminée par le texte généré.
* En règle générale, l’ancre de calque par défaut des calques de texte à redimensionnement automatique n’est *pas* au centre du calque (voir ci-dessous).
* Si `anchor=` ou `origin=` est spécifié pour les calques de texte à redimensionnement automatique, la position du calque de texte est influencée par le contenu du texte.

* Une fois `size=` spécifié, des parties de glyphes de caractères peuvent être rendues en dehors du rectangle du calque.
* `pos=` peut être utilisé dans tous les cas pour repositionner un calque de texte.

## Texte de point (auto-dimensionnement) {#section-db99ec98eb114458b2dbc9911a58f74a}

Le texte de point de style Photoshop est simulé lorsqu’ `textPs=` il est spécifié sans `size=`, `textPath=`ou `textFlowPath=`. La taille du calque est déterminée horizontalement par la largeur du texte rendu et verticalement par l’interligne. Le texte ne sera jamais automatiquement encapsulé.

Si aucune `anchor=` ou `origin=` n&#39;est spécifiée, la première ligne du texte est placée immédiatement au-dessus du calque  le  ; les paragraphes marqués avec `\ql` sont positionnés à droite du calque  , les paragraphes qui incluent `\qr` sont rendus à gauche du  et les paragraphes avec `\qc` sont centrés horizontalement autour du. Les règles standard de positionnement des calques s’appliquent si `anchor=` ou `origin=` sont spécifiées.

Si `color=` est spécifié, il remplit le cadre de sélection du texte généré.

Les commandes RTF suivantes sont ignorées : `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Zone de texte rectangulaire {#section-1d3ab11df26d4004a1a801546756475d}

Si `size=` est spécifié en plus de `textPs=` (sans `textPath=` et `textFlowPath=`), le texte est limité au rectangle spécifié. Le calque est positionné comme d’habitude. Les glyphes de caractères près des bords de la zone de texte peuvent être rendus partiellement en dehors de la zone de texte.

`color=` remplit la région définie par `size=`.

Toutes les commandes RTF sont appliquées comme prévu.

## Zone de texte Hauteur variable {#section-e1233d1c9f8e43218667361dc0c4fd06}

Si vous spécifiez `size=` une hauteur de 0, la zone de texte peut être dimensionnée verticalement pour contenir tout le contenu. La largeur du calque est définie par la largeur du `size=`calque et la hauteur du calque par la hauteur du texte généré. Le calque est positionné comme d’habitude. Les glyphes de caractères près des bords gauche et droit de la zone de texte peuvent être rendus partiellement en dehors de la zone de texte.

`color=` remplit le rectangle défini par la largeur spécifiée `size=` et la hauteur du texte généré.

Les commandes RTF suivantes sont ignorées :

`\vertal*`

## Auto-dimensionnement du texte dans le chemin {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` conjointement avec `textPs=` peut être utilisé pour définir une ou plusieurs régions dans lesquelles le texte doit être enchaîné. `textFlowXPath=` peut être éventuellement spécifié pour exclure le passage du texte dans une ou plusieurs zones. S’ `size=` il n’est pas spécifié, le calque de texte résultant est auto-dimensionné et la taille du calque est déterminée par le cadre de sélection du texte réellement rendu.

Si aucun `origin=` ou `anchor=` n’est spécifié, l’ancre de calque prend par défaut (0,0) l’espace de coordonnées de pixels utilisé pour définir le ou les chemins, garantissant ainsi un positionnement absolu quel que soit le texte généré. Si `anchor=` ou `origin=` sont spécifiés, le calque est positionné par rapport au cadre de sélection (et s’y adapte) du contenu réel rendu.

`color=` remplit le cadre de sélection du texte généré.

Les commandes RTF suivantes sont ignorées :

`\marg*`

## Texte prédimensionné dans le chemin {#section-ed492a8a54414cd4bde360500cec6968}

Si `size=` est spécifié avec `textFlowPath=`, la taille du calque est prédéfinie. (0,0) de l’espace de coordonnées en pixels utilisé pour définir le ou les chemins est situé dans le coin supérieur gauche du rectangle du calque.

Les `textFlowPath=` régions peuvent se trouver en dehors du rectangle du calque. Le texte est toujours distribué et rendu dans toutes les zones de chemin, même si cela entraîne le rendu du texte en dehors du rectangle du calque. `extend=0,0,0,0`peut être utilisé pour recadrer le texte rendu dans le rectangle du calque.

Pour le positionnement des calques, le rectangle du calque est basé sur le rectangle spécifié `size=`, quelle que soit la quantité de texte réellement rendu, même si une partie se trouve en dehors du rectangle du calque. Le positionnement standard des calques s’applique.

`color=` remplit la zone rectangulaire définie par `size=`.

Les commandes RTF suivantes sont ignorées pour `textFlowPath=`:

`\marg*`

## Auto-dimensionnement du texte sur le chemin {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` définit un ou plusieurs chemins sur lesquels le texte spécifié `textPs=` doit être rendu. Lorsque `size=` ce paramètre n’est pas spécifié, le calque de texte résultant est auto-dimensionné. La taille du calque est déterminée par le cadre de sélection du texte généré.

Si aucune `origin=` valeur n’ `anchor=` est spécifiée, l’ancre de calque prend par défaut (0,0) l’espace de coordonnées en pixels utilisé pour définir le chemin d’accès ; la position du texte rendu est fixe, quelle que soit la quantité de texte généré. Si `anchor=` ou `origin=` sont spécifiés, le calque est positionné par rapport au cadre de sélection (et s’y adapte) du contenu réel rendu.

`color=` remplit le cadre de sélection du texte généré.

Les commandes RTF suivantes sont ignorées :

* `\marg*`
* `\hyph*`
* `\vertal*`

Tout texte après le premier `\par` ou `\line` est ignoré.

## Texte prédimensionné sur le chemin {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Si `size=` est spécifié avec `textPath=`, la taille du calque est prédéfinie. (0,0) de l’espace de coordonnées en pixels utilisé pour définir le ou les chemins est situé dans le coin supérieur gauche du rectangle du calque.

Les chemins peuvent être situés partiellement ou entièrement à l’extérieur du rectangle du calque. Le texte est toujours appliqué et rendu le long du chemin entier, même en dehors du rectangle du calque. `extend=0,0,0,0` peut être utilisé pour recadrer le texte rendu dans le rectangle du calque.

Pour le positionnement des calques, le rectangle du calque est basé sur le rectangle spécifié `size=`, même si une partie du texte est rendue en dehors du rectangle du calque. Le positionnement standard des calques s’applique.

`color=` remplit la zone définie par `size=`.

Les commandes RTF suivantes sont ignorées :

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Tout texte après le premier `\par` ou `\line` est ignoré.
