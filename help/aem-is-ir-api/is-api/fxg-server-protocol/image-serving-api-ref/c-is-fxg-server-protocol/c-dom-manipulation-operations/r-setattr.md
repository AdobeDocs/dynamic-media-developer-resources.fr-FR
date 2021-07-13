---
description: Définissez n’importe quel attribut pour un ID d’élément s7 donné.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# setAttr{#setattr}

Définissez n’importe quel attribut pour un s7:elementID donné.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Si un élément de noeud FXG a `s7:elementID` est défini, vous pouvez manipuler les attributs de ce noeud. Vous pouvez définir autant de paires attribut/valeur que vous le souhaitez. Les attributs n’ont pas besoin d’être déjà définis dans le FXG, mais ils doivent être valides pour l’élément node . Toutes les valeurs comprises entre `{}` doivent être placées dans une séquence d’échappement.

## Exemple {#section-9c37470d5f0349e5b0a97291782cb7a6}

Supposons qu’un attribut `s7:elementID="Group1"` soit défini pour un noeud `BitmapGraphic`, ce qui suit est valide :

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Cet exemple définit les valeurs *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* et *[!DNL scaleY]* pour la balise `BitmapGraphic` et remplace toutes les valeurs existantes.
