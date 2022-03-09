---
title: AssetOperationFault
description: Contient des informations sur les conditions d’avertissement ou d’erreur générées lors d’une opération de ressource par lots. Les champs code et raison correspondent aux champs de message d’erreur qui auraient été générés pour l’opération non-batch équivalente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 7%

---

# AssetOperationFault{#assetoperationfault}

Contient des informations sur les conditions d’avertissement ou d’erreur générées lors d’une opération de ressource par lots. Les champs code et raison correspondent aux champs de message d’erreur qui auraient été générés pour l’opération non-batch équivalente.

Syntaxe

## Paramètres {#section-c906f052f43e4785ba46d92b514b0923}

| Nom | Type | Description |
|---|---|---|
| assetHandle | `xsd:string` | Gestionnaire de ressources pour l’opération ayant échoué. |
| code | `xsd:int` | Code de défaillance de l&#39;opération. |
| motif | `xsd:string` | Description ou raison de la défaillance. |
