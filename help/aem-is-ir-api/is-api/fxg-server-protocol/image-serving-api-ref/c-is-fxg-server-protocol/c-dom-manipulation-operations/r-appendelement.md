---
description: Ajoutez du code XML à un ID d’élément Scene7.
solution: Experience Manager
title: appendElement
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---


# appendElement{#appendelement}

Ajoutez du code XML à un identifiant d’élément Scene7.

`appendElement.elementID=<XML>`

Si un élément de noeud FXG est défini avec `s7:elementID`, la valeur `<XML>` est ajoutée en tant qu’élément enfant. `<XML>` doit être codé.

## Exemple {#section-4368570aa198485d91b73b4d0741478f}

Supposons qu&#39;un attribut `s7:elementID="group1"` soit défini pour un noeud Group, les éléments suivants sont valides :

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Cet exemple montre comment ajouter un enfant de graphique de texte à `group1`.
