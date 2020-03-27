---
description: Ajoutez du code XML à un ID d’élément Scene7.
seo-description: Ajoutez du code XML à un ID d’élément Scene7.
seo-title: appendElement
solution: Experience Manager
title: appendElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 062c8288-4517-42a1-9f9f-f3c7bbb4b63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# appendElement{#appendelement}

Ajoutez du code XML à un identifiant d’élément Scene7.

`appendElement.elementID=<XML>`

Si un élément de noeud FXG est `s7:elementID` défini, la `<XML>` valeur est ajoutée en tant qu’élément enfant. The `<XML>` must be encoded.

## Exemple {#section-4368570aa198485d91b73b4d0741478f}

Supposons qu’un `s7:elementID="group1"` attribut soit défini pour un noeud de groupe et que les éléments suivants soient valides :

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Cet exemple montre comment ajouter un enfant de graphique de texte à `group1`.
