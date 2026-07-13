---
description: Assets appartenant à une visionneuse d’images.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
TQID: 'https://experienceleague.adobe.com/53rc6Cq1i15GdzOpBek7ls7ixq4RN8z0OfZMOZsqYWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

Assets appartenant à une visionneuse d’images.

La réinitialisation de page signifie qu’un [!DNL eCatalog] doit démarrer une nouvelle page. `RenderSet` indique qu’il fait partie d’un échantillon `RenderSet`. La valeur est forcée à `true` pour les jeux de `eCatalog` et de `RenderSet`.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| asset | `type:Asset` | Assets dans le tableau de visionneuse d’images. |
| pageReset | `xsd:boolean` | Démarre une nouvelle page. Le paramètre est ignoré et la valeur est forcée à `true` pour les jeux de `eCatalog` et de `RenderSet`. |

