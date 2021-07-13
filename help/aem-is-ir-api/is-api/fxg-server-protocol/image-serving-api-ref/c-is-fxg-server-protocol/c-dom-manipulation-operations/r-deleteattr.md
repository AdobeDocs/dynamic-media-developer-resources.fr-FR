---
description: Supprimez tout attribut pour un ID d’élément s7 donné.
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 1%

---

# deleteAttr{#deleteattr}

Supprimez tout attribut pour un s7:elementID donné.

`deleteAttr.elementID={attributeName%26attributeName}`

Si un élément de noeud FXG a une valeur `s7:elementID` définie, les attributs de ce noeud peuvent être supprimés avec cette commande.

## Exemple {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

Cet exemple supprime les attributs *[!DNL x]*, *[!DNL y]* et *[!DNL visible]* du noeud FXG d’origine.
