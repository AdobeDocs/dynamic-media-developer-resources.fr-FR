---
description: Définition de la cible d’une action de clic dans le navigateur.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 12%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

Définition de la cible d’une action de clic dans le navigateur.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| nom | `xsd:string` | Nom de la définition de zone cliquable. |
| shapeType | `xsd:string` | L’une des valeurs de forme régionale. |
| région | `xsd:string` | Coordonnées de la zone cliquable. Le format est basé sur les attributs de balise `<area>` HTML. |
| action | `xsd:string` | Autres attributs à inclure dans la balise `<area>` de l’HTML, y compris l’URL `href`. |
| activé | `xsd:boolean` | True si la zone cliquable est activée. |
