---
description: d’une action de clic dans le navigateur.
seo-description: d’une action de clic dans le navigateur.
seo-title: Zone cliquable
solution: Experience Manager
title: Zone cliquable
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Zone cliquable{#imagemap}

d’une action de clic dans le navigateur.

Toujours associé à une image. Vous pouvez obtenir un `ImageMap` de `ImageInfo`.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Poignée de zone cliquable. |
| ` *`nom`*` | `xsd:string` | Nom de la zone cliquable. |
| ` *`région`*` | `xsd:string` | Coordonnées de zone cliquable. Le format est basé sur l’attribut de balise HTML `<area>` . |
| ` *`action`*` | `xsd:string` | Autres attributs à inclure dans la balise HTML `<area>` , y compris l’ `href` URL. |
| ` *`shapeType`*` | `xsd:boolean` | Une [!DNL RegionShape] valeur. |
| ` *`position`*` | `xsd:string` | Position au format de l’ `<area>` [!DNL coords] attribut de l’élément HTML. Par exemple: `coords ="0,0,84,128"`. |
| ` *`activé`*` | `xsd:boolean` | True si la zone cliquable est activée. |
| ` *`lastModified`*` | `xsd:dateTime` | Date et heure de la dernière modification de la zone cliquable. |

