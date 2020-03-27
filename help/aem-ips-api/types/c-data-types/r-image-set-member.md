---
description: Fichiers appartenant à une visionneuse d’images.
seo-description: Fichiers appartenant à une visionneuse d’images.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
topic: Scene7 Image Production System API
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageSetMember{#imagesetmember}

Fichiers appartenant à une visionneuse d’images.

La réinitialisation de page signifie qu’un utilisateur [!DNL eCatalog] doit une nouvelle page. `RenderSet` indique qu’il fait partie d’une `RenderSet` nuance. La valeur est forcée à `true` pour `eCatalog` et `RenderSet` pour les ensembles.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`asset`*` | `type:Asset` | Fichiers dans le tableau de la visionneuse d’images. |
| ` *`pageReset`*` | `xsd:boolean` |  une nouvelle page. Le paramètre est ignoré et la valeur est forcée `true` pour `eCatalog` les ensembles et `RenderSet` . |

