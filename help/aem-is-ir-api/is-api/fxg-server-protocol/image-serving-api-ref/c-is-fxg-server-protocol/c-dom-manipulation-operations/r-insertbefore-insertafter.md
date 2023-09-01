---
title: insertBefore,insertAfter
description: Définissez le code XML avant ou après un noeud.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 20d27fa7-e98a-4f85-9e48-5fa9ad3102b7
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 1%

---

# insertBefore,insertAfter{#insertbefore-insertafter}

Définissez le code XML avant ou après un noeud.

`insertBefore=<xml>, insertAfter=<xml>`

Si un élément de noeud FXG comporte une propriété `s7:elementID` défini, vous pouvez ajouter des fragments XML avant ou après ce noeud avec cette commande.

## Exemple {#section-1fc8d4135ef94b60b838391e1568e70e}

Si vous disposez d’une balise Group comme suit :

`<Group visible="true" s7:elementID="inner_shape">`

Ensuite :

`insertBefore.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

Résultats dans :

`<Rect height="75" rotation="0" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" width="75" x="74.354" y="182.762"><fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill></Rect><Group s7:elementID="inner_shape" visible="true">`

`insertAfter.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

Résultats dans :

`<Group s7:elementID="inner_shape" visible="true"> <Rect ai:knockout="0" d:userLabel="Background" height="392.581" visible="true" width="319.953" x="0.75" y="0.75"> <fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill> </Rect>`
