---
title: setElement
description: Définissez XML sur un élément ID s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---

# setElement{#setelement}

Définissez XML sur un s7:elementID.

`setElement.elementID=<XML>`

Si un élément de noeud FXG comporte une propriété `s7:elementID` définie, la variable `<XML>` est remplacée en tant qu’élément enfant. La variable `<XML>` doivent être codées.

## Exemple {#section-f23a998b18994dd3b5d4e1965718db9f}

Supposons qu’une `s7:elementID="group2"` est défini pour un `Group` , ce qui suit est valide :

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Cet exemple supprime tous les enfants du `group2`noeud et le remplace par un nouveau `TextGraphic` noeud enfant.
