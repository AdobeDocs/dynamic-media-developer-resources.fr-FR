---
description: Définissez XML sur un ID d’élément Scene7.
seo-description: Définissez XML sur un ID d’élément Scene7.
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 1%

---


# setElement{#setelement}

Définissez XML sur un identifiant d’élément Scene7.

`setElement.elementID=<XML>`

Si un élément de noeud FXG est défini avec `s7:elementID`, la valeur `<XML>` est remplacée en tant qu’élément enfant. `<XML>` doit être codé.

## Exemple {#section-f23a998b18994dd3b5d4e1965718db9f}

Supposons qu’un attribut `s7:elementID="group2"` soit défini pour un noeud `Group` et que les éléments suivants soient valides :

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Cet exemple montre comment supprimer tous les enfants du noeud `group2`et les remplacer par le nouveau noeud enfant `TextGraphic`.
