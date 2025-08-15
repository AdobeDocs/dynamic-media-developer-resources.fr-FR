---
title: setAttr
description: Définissez n’importe quel attribut pour un ID d’élément s7 donné.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---

# setAttr{#setattr}

Définissez n’importe quel attribut pour un s7:elementID donné.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Si un élément de nœud FXG a une `s7:elementID` valeur définie, vous pouvez manipuler les attributs de ce nœud. Vous pouvez définir autant de paires attribut/valeur que vous le souhaitez. Il n’est pas nécessaire que les attributs soient déjà définis dans le FXG, mais ils doivent être valides pour l’élément de nœud. Toutes les valeurs comprises entre les deux doivent être placées dans `{}` une séquence d’échappement.

## Exemple {#section-9c37470d5f0349e5b0a97291782cb7a6}

Supposons qu’un `s7:elementID="Group1"` attribut est défini pour un `BitmapGraphic` nœud, alors le code suivant est valide :

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Cet exemple définit les variables *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* et *[!DNL scaleY]* pour les `BitmapGraphic` et remplace toutes les valeurs existantes.
