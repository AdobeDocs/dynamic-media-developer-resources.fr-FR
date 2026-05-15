---
title: AssetOperationFault
description: Contient des informations sur les conditions d’avertissement ou d’erreur générées lors d’une opération de ressource par lots. Les champs code et motif correspondent aux champs de message d’erreur qui auraient été déclenchés pour l’opération équivalente hors lot.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
TQID: 'https://experienceleague.adobe.com/LCiMAp-8grDIfCEGX3sF2kBhDamlxZ8iFHT1BjBLkCY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 7%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

Contient des informations sur les conditions d’avertissement ou d’erreur générées lors d’une opération de ressource par lots. Les champs code et motif correspondent aux champs de message d’erreur qui auraient été déclenchés pour l’opération équivalente hors lot.

Syntaxe

## Paramètres {#section-c906f052f43e4785ba46d92b514b0923}

| Nom | Type | Description |
|---|---|---|
| assetHandle | `xsd:string` | Identifiant de ressource pour l’opération ayant échoué. |
| code | `xsd:int` | Code d’erreur d’opération. |
| motif | `xsd:string` | Description ou raison de l’erreur. |
