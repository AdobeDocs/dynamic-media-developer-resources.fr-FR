---
description: Définition de cible pour une action de clic dans le navigateur.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 11%

---


# ImageMapDefinition{#imagemapdefinition}

Définition de cible pour une action de clic dans le navigateur.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`name`*` | `xsd:string` | Nom de la définition de zone cliquable. |
| `*`shapeType`*` | `xsd:string` | L’une des valeurs de forme de région. |
| `*`région`*` | `xsd:string` | Coordonnées de la zone cliquable. Le format est basé sur les attributs de balise HTML `<area>`. |
| `*`action`*` | `xsd:string` | Autres attributs à inclure dans la balise HTML `<area>`, y compris l’URL `href`. |
| `*`activé`*` | `xsd:boolean` | True si la zone cliquable est activée. |

