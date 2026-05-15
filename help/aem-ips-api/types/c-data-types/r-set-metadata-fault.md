---
description: Détails d’avertissement ou d’erreur pour une mise à jour d’utilisation dans une opération batchSetAssetMetadata.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
TQID: 'https://experienceleague.adobe.com/kqC7eTmOZHNIYAn8yTKr-q-rJMQMzqBC9moArFK9no4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 58
ht-degree: 12%

---

# [!DNL SetMetadataFault]{#setmetadatafault}

Détails d’avertissement ou d’erreur pour une mise à jour d’utilisation dans une opération batchSetAssetMetadata.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| assetHandle | `xsd:string` | La ressource dont les métadonnées n’ont pas pu être définies. |
| fieldHandle | `xsd:string` | Gestionnaire du champ de métadonnées dont la valeur a été définie avec succès. |
| code | `xsd:int` | Code d’erreur. |
| motif | `xsd:string` | Description des erreurs (texte brut). |
