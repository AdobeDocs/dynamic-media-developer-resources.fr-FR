---
description: Coordonnées d’emplacement des images renvoyées par l’opération getPhotoshopPath.
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

Coordonnées d’emplacement des images renvoyées par l’opération getPhotoshopPath.

Syntaxe

## Paramètres {#section-59792c446366456d90de7f5875bad1b0}

| Nom | Type | Description |
|---|---|---|
| x0 | `xsd:double` | Coordonnées de l’axe X en haut à gauche. |
| y0 | `xsd:double` | Coordonnées de l’axe y en haut à gauche. |
| x1 | `xsd:double` | Coordonnées de l’axe X en haut à droite. |
| y1 | `xsd:double` | Coordonnées de l’axe y en haut à droite. |
| x2 | `xsd:double` | Coordonnées de l’axe X en bas à droite. |
| y2 | `xsd:double` | Coordonnées de l’axe y en bas à droite. |
| x3 | `xsd:double` | Cooridnate de l’axe X en bas à gauche. |
| y3 | `xsd:double` | Coordonnées de l’axe y en bas à gauche. |

## Exemple {#section-19ed4409ff3a41c9b52a9c9424612927}

Le `PerspectiveQuad` type renvoie les données dans cet ordre :

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
