---
description: Informations sur le log de traitement.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
TQID: 'https://experienceleague.adobe.com/wH0F5TxaTHxn-vP7PTri94WxEa5Bs9Q2-CRnuHdVb3I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 8%

---

# [!DNL JobLogDetail]{#joblogdetail}

Informations sur le log de traitement.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| logMessage | `xsd:string` | Messages du log de traitement. |
| logType | `xsd:string` | Type de fichier journal de traitement. |
| assetName | `xsd:string` | Nom de la ressource dans le log de traitement (facultatif). |
| assetType | `xsd:string` | Choix du type de ressource. |
| assetHandle | `xsd:string` | Descripteur de ressource référencé dans le log de traitement. |
| auxArray | `types:JobLogDetailAuxArray` | Fournit des informations détaillées supplémentaires sur les logs de traitement, en plus des cinq types décrits ci-dessus. |

