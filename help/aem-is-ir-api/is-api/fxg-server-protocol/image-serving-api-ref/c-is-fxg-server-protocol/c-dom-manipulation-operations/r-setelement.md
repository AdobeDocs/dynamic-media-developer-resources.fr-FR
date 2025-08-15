---
title: setElement
description: Définissez XML sur un elementID s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# setElement{#setelement}

Définissez XML sur s7:elementID.

`setElement.elementID=<XML>`

Si un `s7:elementID` est défini pour un élément de nœud FXG, la valeur `<XML>` est remplacée en tant qu’élément enfant. Le `<XML>` doit être encodé.

## Exemple {#section-f23a998b18994dd3b5d4e1965718db9f}

Supposons qu’un attribut `s7:elementID="group2"` soit défini pour un nœud `Group`. Les éléments suivants sont alors valides :

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Cet exemple montre comment supprimer tous les enfants du nœud `group2` et le remplacer par un nouveau nœud enfant `TextGraphic`.
