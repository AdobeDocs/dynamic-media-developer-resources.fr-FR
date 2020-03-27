---
description: Définissez n’importe quel attribut pour un ID d’élément Scene7 donné.
seo-description: Définissez n’importe quel attribut pour un ID d’élément Scene7 donné.
seo-title: setAttr
solution: Experience Manager
title: setAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAttr{#setattr}

Définissez un attribut pour un identifiant d’élément Scene7 donné.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Si un élément de noeud FXG est `s7:elementID` défini, vous pouvez manipuler les attributs de ce noeud. Vous pouvez définir autant de paires attribut/valeur que vous le souhaitez. Les attributs n’ont pas besoin d’être déjà définis dans le fichier FXG, mais ils doivent être valides pour l’élément de noeud. Toutes les valeurs comprises entre `{}` ces deux valeurs doivent être ignorées.

## Exemple {#section-9c37470d5f0349e5b0a97291782cb7a6}

Si un `s7:elementID="Group1"` attribut est défini pour un `BitmapGraphic` noeud, les éléments suivants sont valides :

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Cet exemple montre comment définir les valeurs *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]*, et *[!DNL scaleY]* pour `BitmapGraphic` et remplacer toutes les valeurs existantes.
