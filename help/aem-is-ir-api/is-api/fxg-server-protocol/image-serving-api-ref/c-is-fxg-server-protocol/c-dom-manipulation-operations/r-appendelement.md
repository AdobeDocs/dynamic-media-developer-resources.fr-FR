---
title: Élément appendElement
description: Ajoutez XML à un ID d’élément s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---

# Élément appendElement{#appendelement}

Ajoutez XML à un élément s7:elementID.

`appendElement.elementID=<XML>`

Si une `s7:elementID` valeur est définie pour un élément de nœud FXG, la `<XML>` valeur est ajoutée en tant qu’élément enfant. Le fichier `<XML>` doit être codé.

## Exemple {#section-4368570aa198485d91b73b4d0741478f}

Supposons qu’un `s7:elementID="group1"` attribut est défini pour un nœud Group alors le code suivant est valide :

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Cet exemple ajoute un graphique de texte enfant à `group1`.
