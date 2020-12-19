---
description: Définition de cible pour une action de clic dans le navigateur.
seo-description: Définition de cible pour une action de clic dans le navigateur.
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
topic: Scene7 Image Production System API
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 10%

---


# ImageMapDefinition{#imagemapdefinition}

Définition de cible pour une action de clic dans le navigateur.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`name`*` | `xsd:string` | Nom de la définition de zone cliquable. |
| ` *`shapeType`*` | `xsd:string` | L’une des valeurs de forme de région. |
| ` *`région`*` | `xsd:string` | Coordonnées de la zone cliquable. Le format est basé sur les attributs de balise HTML `<area>`. |
| ` *`action`*` | `xsd:string` | Autres attributs à inclure dans la balise HTML `<area>`, y compris l’URL `href`. |
| ` *`activé`*` | `xsd:boolean` | True si la zone cliquable est activée. |

