---
title: Positionnement du texte
description: Le rendu text= positionne le texte fondamentalement différent du rendu textPs= lorsqu’il est appliqué à des calques prédimensionnés (c’est-à-dire lorsque size= est également spécifié).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Positionnement du texte{#text-positioning}

Le `text=` rendu positionne le texte fondamentalement différent du rendu textPs= lorsqu’il est appliqué à des calques prédimensionnés (c’est-à-dire lorsque size= est également spécifié).

L’auto-dimensionnement `text=`et `textPs=` les calques ont un aspect et un positionnement similaires.

Le `textPs=` permet d’aligner le haut de la cellule de caractères sur le haut de la zone de texte (en supposant `\vertalt`que ), même si des parties des glyphes de texte rendus s’étendent partiellement au-delà des limites de la zone de texte. Les glyphes rendus de certaines polices peuvent également dépasser légèrement les bords gauche et droit de la zone de texte. Pour les applications nécessitant que tout le texte rendu soit contenu dans le rectangle de calque, les commandes RTF `\marg*` peuvent être `textFlowPath=` utilisées pour ajuster la zone de rendu du texte.

En revanche, `text=` décale le texte rendu selon les besoins et garantit que tous les glyphes rendus s’intègrent parfaitement dans la zone de texte spécifiée.

Bien que `text=` peut être légèrement plus facile à utiliser pour des applications simples, `textPs=` offre un positionnement précis indépendamment des polices et des effets de texte.

## Exemples {#section-1b6bdf2ea34447528188ae4e1430ee71}

Les exemples suivants concernent du texte prédimensionné. Le comportement du texte auto-dimensionné est différent.

** `Text=` fournit toujours une marge étroite en haut :**

![Exemple de positionnement de texte une image](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` rend le texte étroitement aligné sur le haut de la zone de texte, ce qui entraîne une légère écrêtage, même pour les polices courantes telles que Arial®:**

![Exemple de positionnement de texte deux Image](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` déplace automatiquement le texte rendu vers le bas pour éviter l’écrêtage :**

![Exemple de positionnement de texte illustré trois](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` ne déplace pas le texte contenant des parties en relief, ce qui entraîne un écrêtage important si le texte se trouve sur le calque 0 :**

![Exemple quatre de positionnement de texte](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Une marge de 10 points (200 twips) en haut rend ce texte sans écrêtage :**

![Exemple de positionnement de texte cinq image](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Le rendu des glyphes de certaines polices de script peut s’étendre considérablement au-delà de la zone de texte :**

![Exemple de positionnement de texte six image](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
