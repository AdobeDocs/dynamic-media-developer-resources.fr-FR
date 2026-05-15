---
description: Coordonnées d’emplacement de l’image renvoyées par l’opération getPhotoshopPath.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
TQID: 'https://experienceleague.adobe.com/jJYhv5-HhU2t1CyVeRVzmIsprZ3xM4ZQtcMDS-Zgt6I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 7%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

Coordonnées d’emplacement de l’image renvoyées par l’opération getPhotoshopPath.

Syntaxe

## Paramètres {#section-59792c446366456d90de7f5875bad1b0}

| Nom | Type | Description |
|---|---|---|
| x0 | `xsd:double` | Coordonnée supérieure gauche de l’axe X. |
| y0 | `xsd:double` | Coordonnée supérieure gauche de l’axe Y. |
| x1 | `xsd:double` | Coordonnée supérieure droite de l’axe X. |
| y1 | `xsd:double` | Coordonnée supérieure droite de l’axe y. |
| x2 | `xsd:double` | Coordonnée inférieure droite de l’axe X. |
| y2 | `xsd:double` | Coordonnée inférieure droite de l’axe y. |
| x3 | `xsd:double` | Coordonnées de l’axe X inférieur gauche. |
| y3 | `xsd:double` | Coordonnée inférieure gauche de l’axe Y. |

## Exemple {#section-19ed4409ff3a41c9b52a9c9424612927}

Le type de `PerspectiveQuad` renvoie les données dans l’ordre suivant :

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
