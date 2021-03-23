---
description: Supprimez tout attribut d’un ID d’élément Scene7 donné.
seo-description: Supprimez tout attribut d’un ID d’élément Scene7 donné.
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 1%

---


# deleteAttr{#deleteattr}

Supprimez tout attribut d’un identifiant d’élément Scene7 donné.

`deleteAttr.elementID={attributeName%26attributeName}`

Si un élément de noeud FXG est défini avec `s7:elementID`, les attributs de ce noeud peuvent être supprimés à l’aide de cette commande.

## Exemple {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

Cet exemple montre comment supprimer les attributs *[!DNL x]*, *[!DNL y]* et *[!DNL visible]* du noeud FXG d&#39;origine.
