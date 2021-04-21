---
description: Coordonnées d’emplacement de l’image renvoyées par l’opération getPhotoshopPath.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 17%

---


# PerspectiveQuad{#perspectivequad}

Coordonnées d’emplacement de l’image renvoyées par l’opération getPhotoshopPath.

Syntaxe

## Paramètres {#section-59792c446366456d90de7f5875bad1b0}

| Nom | Type | Description |
|---|---|---|
| `*`x0`*` | `xsd:double` | Coordonnée supérieure gauche de l’axe X. |
| `*`y0`*` | `xsd:double` | Coordonnée supérieure gauche de l’axe des ordonnées. |
| `*`x1`*` | `xsd:double` | Coordonnée supérieure droite de l’axe X. |
| `*`y1`*` | `xsd:double` | Coordonnée supérieure droite de l’axe y. |
| `*`x2`*` | `xsd:double` | Coordonnée inférieure droite de l’axe X. |
| `*`y2`*` | `xsd:double` | Coordonnée inférieure droite de l’axe y. |
| `*`x3`*` | `xsd:double` | Coordonnée de l&#39;axe X inférieure gauche. |
| `*`y3`*` | `xsd:double` | Coordonnée inférieure gauche de l’axe des ordonnées. |

## Exemple {#section-19ed4409ff3a41c9b52a9c9424612927}

Le type `PerspectiveQuad` renvoie les données dans cet ordre :

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORELIKETHIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)

