---
title: setVal
description: Définissez la valeur du nœud de texte pour s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 1%

---

# setVal{#setval}

Définissez la valeur du nœud de texte pour s7:elementID.

`setVal.elementID= *[!DNL value]*`

Si un `s7:elementID` est défini pour un élément de nœud FXG, la valeur textuelle de ce nœud peut être manipulée.

## Exemple {#section-f574fd66dedd4a219aa537d7bdabea23}

Supposons qu’un attribut `s7:elementID="paragraph1"` soit défini pour un nœud `TextGraphic`. Les éléments suivants sont alors valides :

`&setVal.paragraph=Hello`

Cet exemple montre comment définir la valeur de texte du nœud de paragraphe sur « Hello ».
