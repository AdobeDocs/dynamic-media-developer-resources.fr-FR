---
description: Définissez n’importe quel attribut pour un ID d’élément Scene7 donné.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# setAttr{#setattr}

Définissez n’importe quel attribut pour un identifiant d’élément Scene7 donné.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Si un élément de noeud FXG est défini avec `s7:elementID`, vous pouvez manipuler les attributs de ce noeud. Vous pouvez définir autant de paires attribut/valeur que vous le souhaitez. Les attributs n’ont pas besoin d’être déjà définis dans le fichier FXG, mais ils doivent être valides pour l’élément de noeud. Toutes les valeurs comprises entre `{}` doivent être ignorées.

## Exemple {#section-9c37470d5f0349e5b0a97291782cb7a6}

Supposons qu’un attribut `s7:elementID="Group1"` soit défini pour un noeud `BitmapGraphic`, les éléments suivants sont valides :

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Cet exemple définit les valeurs *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* et *[!DNL scaleY]* pour `BitmapGraphic` et remplace toutes les valeurs existantes.
