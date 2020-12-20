---
description: Définissez la valeur du noeud de texte pour l’ID d’élément Scene7.
seo-description: Définissez la valeur du noeud de texte pour l’ID d’élément Scene7.
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Scene7 Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# setVal{#setval}

Définissez la valeur du noeud de texte pour s7:elementID.

`setVal.elementID= *[!DNL value]*`

Si un élément de noeud FXG est défini avec `s7:elementID`, la valeur de texte de ce noeud peut être manipulée.

## Exemple {#section-f574fd66dedd4a219aa537d7bdabea23}

Supposons qu’un attribut `s7:elementID="paragraph1"` soit défini pour un noeud `TextGraphic` et que les éléments suivants soient valides :

`&setVal.paragraph=Hello`

Cet exemple montre comment définir la valeur de texte du noeud de paragraphe sur &quot;Hello&quot;.
