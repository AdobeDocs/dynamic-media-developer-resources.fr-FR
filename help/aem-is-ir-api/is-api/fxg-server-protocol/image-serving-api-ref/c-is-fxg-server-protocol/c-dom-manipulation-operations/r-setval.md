---
title: setVal
description: Définissez la valeur du nœud de texte pour s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
TQID: 'https://experienceleague.adobe.com/bwE12rWee56rVQDuctPsmq5TUwVJy39HNUff-ZYuybM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
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
