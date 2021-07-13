---
description: Définissez XML sur un élément ID s7.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---

# setElement{#setelement}

Définissez XML sur un s7:elementID.

`setElement.elementID=<XML>`

Si un élément de noeud FXG a une valeur `s7:elementID` définie, la valeur `<XML>` est remplacée en tant qu’élément enfant. `<XML>` doit être codé.

## Exemple {#section-f23a998b18994dd3b5d4e1965718db9f}

Supposons qu’un attribut `s7:elementID="group2"` soit défini pour un noeud `Group`, ce qui suit est valide :

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Cet exemple supprime tous les enfants du noeud `group2`et le remplace par le nouveau noeud enfant `TextGraphic`.
