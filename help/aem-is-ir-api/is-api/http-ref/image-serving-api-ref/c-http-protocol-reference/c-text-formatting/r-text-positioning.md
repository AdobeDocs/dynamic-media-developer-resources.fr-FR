---
title: Position du texte
description: text= renderer positionne le texte de manière fondamentalement différente de textPs= renderer lorsqu’il est appliqué aux calques prédimensionnés (c’est-à-dire lorsque size= est également spécifié).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Position du texte{#text-positioning}

Le moteur de rendu `text=` positionne le texte fondamentalement différent du rendu textPs= lorsqu’il est appliqué aux calques prédimensionnés (c’est-à-dire lorsque size= est également spécifié).

Les calques `text=`d’auto-dimensionnement et `textPs=` ont une apparence et un positionnement similaires.

`textPs=` aligne le haut de la cellule de caractère avec le haut de la zone de texte (en supposant `\vertalt`), même si des parties des glyphes de texte rendu s’étendent partiellement en dehors des limites de la zone de texte. Les glyphes rendus de certaines polices peuvent également se propager légèrement au-delà des bords gauche et droit de la zone de texte. Pour les applications exigeant que tout le texte rendu soit contenu dans le rectangle du calque, les commandes RTF `\marg*` ou `textFlowPath=` peuvent être utilisées pour ajuster la zone de rendu du texte.

En revanche, `text=` déplace le texte rendu selon les besoins et garantit que tous les glyphes rendus correspondent entièrement à la zone de texte spécifiée.

`text=` peut s’avérer un peu plus facile à utiliser pour les applications simples, `textPs=` offre un positionnement précis, indépendamment des faces de police et des effets de texte.

## Exemples {#section-1b6bdf2ea34447528188ae4e1430ee71}

Les exemples suivants concernent du texte prédimensionné. Le comportement du texte auto-dimensionné est différent.

** `Text=` fournit toujours une marge étroite en haut :**

![Exemple de positionnement de texte d’une image](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` effectue le rendu du texte étroitement aligné en haut de la zone de texte, ce qui se traduit par un léger détourage, même pour les polices courantes telles que Arial®:**

![Exemple de positionnement de texte deux images](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` déplace automatiquement le texte rendu vers le bas pour éviter l’écrêtage :**

![Exemple de positionnement de texte trois images](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` ne déplace pas le texte contenant des parties élevées, ce qui entraîne un détourage significatif si le texte se trouve sur le calque 0 :**

![Exemple de positionnement de texte quatre images](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Une marge de 10 pt (200 twips) dans la partie supérieure affiche ce texte sans écrêtage :**

![Exemple de positionnement de texte cinq images](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Les glyphes rendus de certaines polices de script peuvent s’étendre de manière significative en dehors de la zone de texte :**

![Exemple de positionnement de texte six images](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
