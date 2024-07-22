---
description: Ciblez une action de clic dans le navigateur.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---

# [!DNL ImageMap]{#imagemap}

Ciblez une action de clic dans le navigateur.

Toujours associée à une image. Vous pouvez obtenir une cible `ImageMap` de `ImageInfo`.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| imageMapHandle | `xsd:string` | Poignée de zone cliquable. |
| [!DNL name] | `xsd:string` | Nom de la zone cliquable. |
| [!DNL region] | `xsd:string` | Coordonnées de la zone cliquable. Le format est basé sur l’attribut de balise `<area>` HTML. |
| [!DNL action] | `xsd:string` | Autres attributs à inclure dans la balise `<area>` de l’HTML, y compris l’URL `href`. |
| shapeType | `xsd:boolean` | Une valeur [!DNL RegionShape]. |
| [!DNL position] | `xsd:string` | Position au format de l’attribut [!DNL coords] de l’élément `<area>` de l’HTML. Par exemple : `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True si la zone cliquable est activée. |
| lastModified | `xsd:dateTime` | Date et heure de la dernière modification de la zone cliquable. |
