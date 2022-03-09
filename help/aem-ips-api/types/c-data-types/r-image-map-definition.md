---
description: Définition de la cible d’une action de clic dans le navigateur.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 12%

---

# ImageMapDefinition{#imagemapdefinition}

Définition de la cible d’une action de clic dans le navigateur.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| name | `xsd:string` | Nom de la définition de zone cliquable. |
| shapeType | `xsd:string` | Une des valeurs de forme régionale. |
| région | `xsd:string` | Coordonnées de la zone cliquable. Le format est basé sur le HTML `<area>` attributs de balise. |
| action | `xsd:string` | Autres attributs à inclure dans le HTML `<area>` , y compris la balise `href` URL. |
| activé | `xsd:boolean` | True si la zone cliquable est activée. |
