---
description: textPs= prend en charge plusieurs modèles d’utilisation décrits dans cette section.
solution: Experience Manager
title: Calques de texte
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
TQID: 'https://experienceleague.adobe.com/cIgicI7IPJKVWkhlyocD7g7nuXbJXaTAborYvt3Muyg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 904
ht-degree: 0%

---

# Calques de texte{#text-layers}

textPs= prend en charge plusieurs modèles d’utilisation décrits dans cette section.

>[!NOTE]
>
>Cette section ne s’applique pas aux `text=`.

Les règles et définitions communes sont les suivantes :

* Les calques de texte à redimensionnement automatique sont des calques qui n’incluent pas de commande `size=` ou pour lesquels `size=0,0` est spécifié.

* La taille des calques de texte à redimensionnement automatique est déterminée par le texte réel rendu.
* L’ancre de calque par défaut des calques de texte à redimensionnement automatique est généralement *pas* au centre du calque (voir ci-dessous).
* Si `anchor=` ou `origin=` est spécifié pour les calques de texte à redimensionnement automatique, la position du calque de texte est influencée par le contenu du texte.

* Lorsque `size=` est spécifié, des parties de glyphes de caractères peuvent être rendues en dehors du rectangle du calque.
* `pos=` permet dans tous les cas de repositionner un calque de texte.

## Texte du point (auto-dimensionnement) {#section-db99ec98eb114458b2dbc9911a58f74a}

Le texte de point de style Photoshop est simulé lorsque la `textPs=` est spécifiée sans `size=`, `textPath=` ou `textFlowPath=`. La taille du calque est déterminée horizontalement par la largeur du texte rendu et verticalement par l’espacement des lignes. Le texte n’est jamais automatiquement renvoyé à la ligne.

Si ni `anchor=` ni `origin=` ne sont spécifiés, la première ligne du texte est positionnée immédiatement au-dessus de l’origine du calque ; les paragraphes marqués d’`\ql` sont positionnés à droite de l’origine du calque, les paragraphes contenant des `\qr` sont rendus à gauche de l’origine et les paragraphes avec des `\qc` sont centrés horizontalement autour de l’origine. Les règles de positionnement de calque standard s&#39;appliquent si `anchor=` ou `origin=` sont spécifiés.

Si `color=` est spécifié, il remplit le cadre de sélection du texte réel rendu.

Les commandes RTF suivantes sont ignorées : `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Zone de texte rectangulaire {#section-1d3ab11df26d4004a1a801546756475d}

Si `size=` est spécifié en plus de `textPs=` (sans `textPath=` ni `textFlowPath=`), le texte est limité au rectangle spécifié. La couche est positionnée comme d&#39;habitude. Les glyphes de caractères à proximité des bords de la zone de texte peuvent être rendus partiellement en dehors de la zone de texte.

`color=` remplit la région définie par `size=`.

Toutes les commandes RTF sont appliquées comme prévu.

## Zone de texte de hauteur variable {#section-e1233d1c9f8e43218667361dc0c4fd06}

La spécification d’`size=` avec une hauteur de 0 permet de dimensionner la zone de texte verticalement pour s’adapter à tout le contenu. La largeur du calque est définie par la largeur de `size=` et la hauteur du calque par la hauteur du texte rendu réel. La couche est positionnée comme d&#39;habitude. Les glyphes de caractères près des bords gauche et droit de la zone de texte peuvent être rendus partiellement en dehors de la zone de texte.

`color=` remplit le rectangle défini par la largeur spécifiée avec `size=` et la hauteur du texte réel rendu.

Les commandes RTF suivantes sont ignorées :

`\vertal*`

## Texte à redimensionnement automatique dans le chemin d’accès {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` peut être utilisé conjointement avec `textPs=` pour définir une ou plusieurs régions dans lesquelles le texte doit être placé. `textFlowXPath=` peut être spécifié de manière facultative pour empêcher le texte de s’écouler dans une ou plusieurs zones. Si `size=` n’est pas spécifié, le calque de texte obtenu s’auto-dimensionne et la taille du calque est déterminée par le cadre de sélection du texte réellement rendu.

Si ni `origin=` ni `anchor=` ne sont spécifiés, l’ancre de calque est définie par défaut sur (0,0) de l’espace des coordonnées des pixels utilisé pour définir le ou les chemins, assurant ainsi un positionnement absolu quel que soit le texte rendu. Si des `anchor=` ou des `origin=` sont spécifiés, le calque est positionné par rapport au cadre de sélection du contenu réel rendu et s’y adapte.

`color=` remplit le cadre de sélection du texte réel rendu.

Les commandes RTF suivantes sont ignorées :

`\marg*`

## Texte pré-dimensionné dans le chemin {#section-ed492a8a54414cd4bde360500cec6968}

Si `size=` est spécifié avec `textFlowPath=`, la taille du calque est prédéfinie. (0,0) de l’espace de coordonnées des pixels utilisé pour définir le(s) chemin(s) se trouve dans le coin supérieur gauche du rectangle du calque.

Les régions `textFlowPath=` peuvent être situées à l&#39;extérieur du rectangle de calque. Le texte est toujours distribué et rendu dans toutes les zones du tracé, même si cela entraîne un rendu du texte en dehors du rectangle du calque. `extend=0,0,0,0`peut être utilisé pour recadrer le texte rendu dans le rectangle de calque.

À des fins de positionnement de calque, le rectangle de calque est basé sur le `size=` spécifié, quelle que soit la quantité de texte effectivement rendue, même si une partie de celui-ci se trouve en dehors du rectangle de calque. Le positionnement standard des calques s’applique.

`color=` remplit la zone rectangulaire définie par `size=`.

Les commandes RTF suivantes sont ignorées pour `textFlowPath=` :

`\marg*`

## Texte à redimensionnement automatique sur le chemin d’accès {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` définit un ou plusieurs chemins d’accès sur lesquels le texte spécifié avec `textPs=` doit être rendu. Lorsque `size=` n’est pas spécifié, le calque de texte obtenu s’auto-dimensionne. La taille du calque est déterminée par le cadre de sélection du texte réel rendu.

Si ni `origin=` ni `anchor=` ne sont spécifiés, l’ancre de calque est définie par défaut sur (0,0) de l’espace de coordonnées des pixels utilisé pour définir le tracé ; la position du texte rendu est fixe, quelle que soit la quantité de texte rendue. Si des `anchor=` ou des `origin=` sont spécifiés, le calque est positionné par rapport au cadre de sélection du contenu réel rendu et s’y adapte.

`color=` remplit le cadre de sélection du texte réel rendu.

Les commandes RTF suivantes sont ignorées :

* `\marg*`
* `\hyph*`
* `\vertal*`

Tout texte postérieur au premier `\par` ou `\line` est ignoré.

## Texte pré-dimensionné sur le chemin {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Si `size=` est spécifié avec `textPath=`, la taille du calque est prédéfinie. (0,0) de l’espace de coordonnées des pixels utilisé pour définir le(s) chemin(s) se trouve dans le coin supérieur gauche du rectangle du calque.

Les chemins peuvent être situés partiellement ou entièrement à l&#39;extérieur du rectangle de calque. Le texte est toujours appliqué et rendu le long du tracé complet, même s’il se trouve en dehors du rectangle du calque. Vous pouvez utiliser `extend=0,0,0,0` pour recadrer le texte rendu dans le rectangle du calque.

Pour le positionnement du calque, le rectangle de calque est basé sur le `size=` spécifié, même si une partie du texte est rendue en dehors du rectangle de calque. Le positionnement standard des calques s’applique.

`color=` remplit la zone définie par `size=`.

Les commandes RTF suivantes sont ignorées :

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Tout texte postérieur au premier `\par` ou `\line` est ignoré.
