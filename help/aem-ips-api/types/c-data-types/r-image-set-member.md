---
description: Fichiers appartenant à une visionneuse d’images.
seo-description: Fichiers appartenant à une visionneuse d’images.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
topic: Dynamic Media Image Production System API
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 6%

---


# ImageSetMember{#imagesetmember}

Fichiers appartenant à une visionneuse d’images.

La réinitialisation de page signifie qu’une [!DNL eCatalog] doit début une nouvelle page. `RenderSet` indique qu’il fait partie d’une  `RenderSet` nuance. La valeur est forcée à `true` pour les ensembles `eCatalog` et `RenderSet`.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`asset`*` | `type:Asset` | Fichiers du tableau de visionneuse d’images. |
| `*`pageReset`*` | `xsd:boolean` | Début une nouvelle page. Le paramètre est ignoré et la valeur est forcée à `true` pour les ensembles `eCatalog` et `RenderSet`. |

