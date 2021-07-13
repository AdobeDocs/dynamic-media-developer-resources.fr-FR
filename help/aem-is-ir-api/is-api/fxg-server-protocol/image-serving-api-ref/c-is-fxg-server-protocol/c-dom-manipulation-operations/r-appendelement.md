---
description: Ajoutez du code XML à un ID d’élément s7.
solution: Experience Manager
title: appendElement
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# appendElement{#appendelement}

Ajoutez du code XML à un s7:elementID.

`appendElement.elementID=<XML>`

Si un élément de noeud FXG a une valeur `s7:elementID` définie, la valeur `<XML>` est ajoutée en tant qu’élément enfant. `<XML>` doit être codé.

## Exemple {#section-4368570aa198485d91b73b4d0741478f}

Supposons qu’un attribut `s7:elementID="group1"` soit défini pour un noeud Groupe , ce qui suit est valide :

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Cet exemple ajoute un enfant graphique de texte à `group1`.
