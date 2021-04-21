---
description: Définissez XML sur un ID d’élément Scene7.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '71'
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
