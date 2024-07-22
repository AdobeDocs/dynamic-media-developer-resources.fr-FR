---
description: Coordonnées de l’emplacement de l’image renvoyées par l’opération getPhotoshopPath.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 8%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

Coordonnées de l’emplacement de l’image renvoyées par l’opération getPhotoshopPath.

Syntaxe

## Paramètres {#section-59792c446366456d90de7f5875bad1b0}

| Nom | Type | Description |
|---|---|---|
| x0 | `xsd:double` | Coordonnée de l’axe X supérieure gauche. |
| y0 | `xsd:double` | Coordonnée de l’axe Y supérieure gauche. |
| x1 | `xsd:double` | Coordonnée de l’axe X supérieur droit. |
| y1 | `xsd:double` | Coordonnée de l’axe y supérieure droite. |
| x2 | `xsd:double` | Coordonnée inférieure droite de l’axe X. |
| y2 | `xsd:double` | Coordonnée inférieure droite de l’axe Y. |
| x3 | `xsd:double` | Coordonnée de l’axe X inférieur gauche. |
| y3 | `xsd:double` | Coordonnée de l’axe Y inférieur gauche. |

## Exemple {#section-19ed4409ff3a41c9b52a9c9424612927}

Le type `PerspectiveQuad` renvoie les données dans l’ordre suivant :

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
