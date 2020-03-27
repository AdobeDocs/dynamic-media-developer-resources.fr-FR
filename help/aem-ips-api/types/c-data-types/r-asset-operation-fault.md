---
description: Contient des informations sur les conditions d’avertissement ou d’erreur générées lors d’une opération de fichier par lot. Les champs code et motif correspondent aux champs de message d’erreur qui auraient été générés pour l’opération non par lot équivalente.
seo-description: Contient des informations sur les conditions d’avertissement ou d’erreur générées lors d’une opération de fichier par lot. Les champs code et motif correspondent aux champs de message d’erreur qui auraient été générés pour l’opération non par lot équivalente.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Scene7 Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetOperationFault{#assetoperationfault}

Contient des informations sur les conditions d’avertissement ou d’erreur générées lors d’une opération de fichier par lot. Les champs code et motif correspondent aux champs de message d’erreur qui auraient été générés pour l’opération non par lot équivalente.

Syntaxe

## Paramètres {#section-c906f052f43e4785ba46d92b514b0923}

| Nom | Type | Description |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Handle de ressource pour l’opération ayant échoué. |
| ` *`code`*` | `xsd:int` | Code d&#39;erreur d&#39;opération. |
| ` *`motif`*` | `xsd:string` | Description ou raison de l’erreur. |

