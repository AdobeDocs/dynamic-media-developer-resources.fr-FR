---
description: Ciblez une action de clic dans le navigateur.
solution: Experience Manager
title: Zone cliquable
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 12%

---

# Zone cliquable{#imagemap}

Ciblez une action de clic dans le navigateur.

Toujours associée à une image. Vous pouvez obtenir une cible `ImageMap` à partir de `ImageInfo`.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Poignée de zone cliquable. |
| `*`name`*` | `xsd:string` | Nom de la zone cliquable. |
| `*`région`*` | `xsd:string` | Coordonnées de la zone cliquable. Le format est basé sur l’attribut de balise HTML `<area>` . |
| `*`action`*` | `xsd:string` | Autres attributs à inclure dans la balise `<area>` HTML, y compris l’URL `href`. |
| `*`shapeType`*` | `xsd:boolean` | Valeur [!DNL RegionShape]. |
| `*`position`*` | `xsd:string` | Position au format de l’attribut `<area>` de l’élément HTML [!DNL coords]. Par exemple: `coords ="0,0,84,128"`. |
| `*`activé`*` | `xsd:boolean` | True si la zone cliquable est activée. |
| `*`lastModified`*` | `xsd:dateTime` | Date et heure de la dernière modification de la zone cliquable. |
