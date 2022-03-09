---
description: Ressources appartenant à une visionneuse d’images.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 7%

---

# ImageSetMember{#imagesetmember}

Ressources appartenant à une visionneuse d’images.

La réinitialisation de la page signifie qu’une [!DNL eCatalog] doit commencer une nouvelle page. `RenderSet` indique qu’il fait partie d’une `RenderSet` échantillon. La valeur est forcée à `true` pour `eCatalog` et `RenderSet` définit.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| asset | `type:Asset` | Ressources dans le tableau de la visionneuse d’images. |
| pageReset | `xsd:boolean` | Commence une nouvelle page. Le paramètre est ignoré et la valeur est forcée à `true` pour `eCatalog` et `RenderSet` définit. |
