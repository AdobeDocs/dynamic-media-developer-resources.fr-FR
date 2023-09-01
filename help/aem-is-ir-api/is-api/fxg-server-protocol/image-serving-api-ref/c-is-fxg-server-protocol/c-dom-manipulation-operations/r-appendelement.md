---
title: appendElement
description: Ajoutez du code XML à un ID d’élément s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---

# appendElement{#appendelement}

Ajoutez du code XML à un s7:elementID.

`appendElement.elementID=<XML>`

Si un élément de noeud FXG comporte une propriété `s7:elementID` définie, la variable `<XML>` est ajoutée en tant qu’élément enfant. La variable `<XML>` doivent être codées.

## Exemple {#section-4368570aa198485d91b73b4d0741478f}

Supposons qu’une `s7:elementID="group1"` est défini pour un noeud Group , puis les éléments suivants sont valides :

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Cet exemple ajoute un enfant graphique de texte à `group1`.
