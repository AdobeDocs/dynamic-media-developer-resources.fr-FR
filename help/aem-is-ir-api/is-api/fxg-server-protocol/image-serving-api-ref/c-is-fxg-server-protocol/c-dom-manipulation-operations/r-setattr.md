---
title: setAttr
description: Définissez n’importe quel attribut pour un elementID s7 donné.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
TQID: 'https://experienceleague.adobe.com/0O1uOLXsh-5PkBnXugpQYJHDAZep49WO3AA4hjClODk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 1%

---

# setAttr{#setattr}

Définissez n’importe quel attribut pour un s7:elementID donné.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Si un `s7:elementID` est défini pour un élément de nœud FXG, vous pouvez manipuler les attributs de ce nœud. Vous pouvez définir autant de paires attribut/valeur que vous le souhaitez. Les attributs n’ont pas besoin d’être déjà définis dans le FXG, mais ils doivent être valides pour l’élément de nœud . Toutes les valeurs comprises entre `{}` doivent être placées dans une séquence d’échappement.

## Exemple {#section-9c37470d5f0349e5b0a97291782cb7a6}

Supposons qu’un attribut `s7:elementID="Group1"` soit défini pour un nœud `BitmapGraphic`, les éléments suivants sont valides :

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Cet exemple montre comment définir les *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* et *[!DNL scaleY]* de la `BitmapGraphic` et remplacer toutes les valeurs existantes.
