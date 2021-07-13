---
description: Définissez les attributs sur l’élément racine FXG.
solution: Experience Manager
title: setAttr.rootElement
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 47bd947f-c078-4fd3-99cb-5ef48ea3e05e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 2%

---

# setAttr.rootElement{#setattr-rootelement}

Définissez les attributs sur l’élément racine FXG.

` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

Cette commande peut manipuler les attributs de l’élément racine.

## Exemple {#section-2758a6e316c34b99b13b02147e5973bb}

Si nous disposons de l’élément racine suivant :

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

Après avoir appliqué la commande suivante :

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

L’élément racine est maintenant remplacé par ce qui suit :

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">`
