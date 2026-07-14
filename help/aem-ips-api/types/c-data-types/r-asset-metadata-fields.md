---
title: AssetMetadataFields
description: Renvoie des définitions de champ de métadonnées pour les types de ressources spécifiés.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
TQID: 'https://experienceleague.adobe.com/U9JVe27HBTMtlBXmwDnkVAOaVfsBspa5r5fvnQl-h58'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 47
ht-degree: 10%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

Renvoie des définitions de champ de métadonnées pour les types de ressources spécifiés.

Syntaxe

## Paramètres {#section-5ad771540c5f40c187b35e34aac19305}

| Nom | Type | Description |
|---|---|---|
| assetType | `xsd:string` | Type de ressource associé aux définitions de champ (voir « Types de ressources » pour les valeurs). |
| fieldArray | `types:MetadataFieldArray` | Tableau de définitions de champs de métadonnées associées au type de ressource spécifié dans `assetType`. |

