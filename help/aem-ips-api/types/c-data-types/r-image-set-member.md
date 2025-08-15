---
description: Assets appartenant à une visionneuse d’images.
solution: Experience Manager
title: Membre du jeu d’images
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

Assets appartenant à une visionneuse d’images.

La réinitialisation de page signifie qu’une [!DNL eCatalog] doit commencer une nouvelle page. `RenderSet` indique qu’il fait partie d’un `RenderSet` échantillon. La valeur est forcée à `true` pour `eCatalog` et `RenderSet` définit.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| asset | `type:Asset` | Assets dans le tableau de la visionneuse d’images. |
| Réinitialisation de la page | `xsd:boolean` | Commence une nouvelle page. Le paramètre est ignoré et la valeur est forcée à `true` for `eCatalog` et `RenderSet` sets. |
