---
description: Le rendu text= positionne le texte fondamentalement différent du rendu textPs= lorsqu’il est appliqué aux calques prédimensionnés (c’est-à-dire lorsque size= est également spécifié).
seo-description: Le rendu text= positionne le texte fondamentalement différent du rendu textPs= lorsqu’il est appliqué aux calques prédimensionnés (c’est-à-dire lorsque size= est également spécifié).
seo-title: Positionnement du texte
solution: Experience Manager
title: Positionnement du texte
topic: Scene7 Image Serving - Image Rendering API
uuid: 77289c50-2f3a-4486-8274-eecfd6e5452f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Positionnement du texte{#text-positioning}

Le rendu text= positionne le texte fondamentalement différent du rendu textPs= lorsqu’il est appliqué aux calques prédimensionnés (c’est-à-dire lorsque size= est également spécifié).

L’auto-dimensionnement `text=`et `textPs=` les calques ont un aspect et un positionnement similaires.

`textPs=` aligne le haut de la cellule de caractère sur le haut de la zone de texte (en supposant `\vertalt`), même si cela entraîne l’extension partielle de certaines parties des glyphes de texte rendus en dehors du cadre de la zone de texte. Les glyphes rendus de certaines polices peuvent également dépasser légèrement les bords gauche et droit de la zone de texte. Pour les applications exigeant que tout le texte rendu soit contenu dans le rectangle du calque, les commandes RTF `\marg*` ou `textFlowPath=` peuvent être utilisées pour ajuster la zone de rendu du texte.

En revanche, `text=` décalera le texte rendu selon les besoins et garantira que tous les glyphes rendus s’intègrent parfaitement dans la zone de texte indiquée.

Bien qu&#39; `text=` il soit un peu plus facile à utiliser pour des applications simples, `textPs=`   un positionnement précis, indépendant des polices et des effets de texte.

## Exemples {#section-1b6bdf2ea34447528188ae4e1430ee71}

Les exemples suivants concernent le texte prédimensionné. Le comportement du texte à redimensionnement automatique est différent.

** `Text=` fournit toujours une marge étroite en haut :**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` effectue le rendu du texte étroitement aligné en haut de la zone de texte, ce qui peut entraîner un léger écrêtage, même pour les polices courantes telles que Arial :**

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` décalera automatiquement le texte rendu vers le bas pour éviter l’écrêtage :**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` ne déplace pas le texte contenant des portions surélevées, ce qui entraîne un rognage important si le texte se trouve sur le calque 0 :**

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Une marge de 10 pt (200 twips) en haut rend ce texte sans écrêtage :**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Les glyphes rendus de certaines polices de script peuvent s’étendre de manière significative en dehors de la zone de texte :**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
