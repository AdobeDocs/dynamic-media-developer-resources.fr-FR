---
description: Ressources appartenant à une visionneuse d’images.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Visionneuses d’images
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 6%

---

# ImageSetMember{#imagesetmember}

Ressources appartenant à une visionneuse d’images.

La réinitialisation de la page signifie qu’une [!DNL eCatalog] doit commencer une nouvelle page. `RenderSet` indique qu’il fait partie d’un  `RenderSet` échantillon. La valeur est forcée à `true` pour les ensembles `eCatalog` et `RenderSet`.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`asset`*` | `type:Asset` | Ressources dans le tableau de la visionneuse d’images. |
| `*`pageReset`*` | `xsd:boolean` | Commence une nouvelle page. Le paramètre est ignoré et la valeur est forcée à `true` pour les jeux `eCatalog` et `RenderSet`. |
