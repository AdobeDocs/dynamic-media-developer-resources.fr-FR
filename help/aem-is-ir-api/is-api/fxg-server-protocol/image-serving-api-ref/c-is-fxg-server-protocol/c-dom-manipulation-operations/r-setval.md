---
description: Définissez la valeur du noeud de texte pour l’ID d’élément Scene7.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
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
