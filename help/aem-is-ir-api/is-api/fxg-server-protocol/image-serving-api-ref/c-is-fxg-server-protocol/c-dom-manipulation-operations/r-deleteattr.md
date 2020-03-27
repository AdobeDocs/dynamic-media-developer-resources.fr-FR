---
description: Supprimez tout attribut d’un ID d’élément Scene7 donné.
seo-description: Supprimez tout attribut d’un ID d’élément Scene7 donné.
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteAttr{#deleteattr}

Supprimez tout attribut d’un identifiant d’élément Scene7 donné.

`deleteAttr.elementID={attributeName%26attributeName}`

Si un élément de noeud FXG est `s7:elementID` défini, les attributs de ce noeud peuvent être supprimés avec cette commande.

## Exemple {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

Cet exemple montre comment supprimer les attributs *[!DNL x]*, *[!DNL y]* et *[!DNL visible]* du noeud FXG d&#39;origine.
