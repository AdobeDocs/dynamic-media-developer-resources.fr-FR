---
description: Définissez le code XML avant ou après un noeud.
seo-description: Définissez le code XML avant ou après un noeud.
seo-title: insertBefore,insertAfter
solution: Experience Manager
title: insertBefore,insertAfter
topic: Scene7 Image Serving - Image Rendering API
uuid: 5ac0f675-333b-4f85-abe0-642cf96de425
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 3%

---


# insertBefore,insertAfter{#insertbefore-insertafter}

Définissez le code XML avant ou après un noeud.

`insertBefore=<xml>, insertAfter=<xml>`

Si un élément de noeud FXG possède une valeur `s7:elementID` définie, nous pouvons ajouter des fragments XML avant ou après ce noeud avec cette commande.

## Exemple {#section-1fc8d4135ef94b60b838391e1568e70e}

Si nous possédons une balise Group comme celle-ci :

`<Group visible="true" s7:elementID="inner_shape">`

ensuite:

`insertBefore.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

donne :

`<Rect height="75" rotation="0" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" width="75" x="74.354" y="182.762"><fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill></Rect><Group s7:elementID="inner_shape" visible="true">`

`insertAfter.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

donne :

`<Group s7:elementID="inner_shape" visible="true"> <Rect ai:knockout="0" d:userLabel="Background" height="392.581" visible="true" width="319.953" x="0.75" y="0.75"> <fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill> </Rect>`
