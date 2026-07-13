---
description: Propriétés de la vue Calque.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
TQID: 'https://experienceleague.adobe.com/cx-B-BmcEP6vefJY5tsrNMZcwWIKM-pW0CYfP7BjxMM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 46
ht-degree: 13%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

Propriétés de la vue Calque.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| url | `xsd:string` | URL du serveur d’images représentant le modèle. Combine les champs `urlModifier` et `urlPostAp- plyModifier`. |
| urlModifier | `xsd:string` | Commande de protocole de diffusion d’image à appliquer avant la commande request ou `urlPostApplyModifier`. |
| urlPostApplyModifier | `xsd:string` | Image diffusant les commandes de protocole à appliquer après les commandes `urlModifier` et request. |

