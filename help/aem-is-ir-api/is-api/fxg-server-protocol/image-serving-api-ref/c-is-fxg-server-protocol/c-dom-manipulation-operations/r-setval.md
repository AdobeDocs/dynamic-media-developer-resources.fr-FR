---
description: Définissez la valeur de noeud de texte pour l’ID d’élément s7.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---

# setVal{#setval}

Définissez la valeur de noeud de texte pour s7:elementID.

`setVal.elementID= *[!DNL value]*`

Si un `s7:elementID` est défini pour un élément de noeud FXG, la valeur de texte de ce noeud peut être manipulée.

## Exemple {#section-f574fd66dedd4a219aa537d7bdabea23}

Supposons qu’un attribut `s7:elementID="paragraph1"` soit défini pour un noeud `TextGraphic`, ce qui suit est valide :

`&setVal.paragraph=Hello`

Cet exemple définit la valeur de texte du noeud de paragraphe sur &quot;Hello&quot;.
