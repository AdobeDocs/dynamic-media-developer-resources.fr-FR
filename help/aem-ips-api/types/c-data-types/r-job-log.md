---
description: Journal des tâches après l’exécution de la tâche.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 3%

---


# JobLog{#joblog}

Journal des tâches après l’exécution de la tâche.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Poignée de société. |
| `*`jobHandle`*` | `xsd:string` | Poignée de tâche. |
| `*`jobName`*` | `xsd:string` | Nom de la tâche. |
| `*`initialJobName`*` | `xsd:string` | Nom d’origine envoyé pour la tâche avec `submitJob`. |
| `*`submitUserEmail`*` | `xsd:string` | Adresse électronique de l’utilisateur qui a envoyé la tâche. |
| `*`logType`*` | `xsd:string` | Choix des types de journaux de tâches. |
| `*`jobSubType`*` | `xsd:string` | Informations supplémentaires sur la tâche. |
| `*`startDate`*` | `xsd:dateTime` | Date, heure et fuseau horaire début de la tâche. |
| `*`endDate`*` | `xsd:dateTime` | Date, heure et fuseau horaire de fin de la tâche. |
| `*`description`*` | `xsd:string` | Description de la tâche telle que spécifiée à l&#39;origine dans `submitJob`. |
| `*`fileSuccessCount`*` | `xsd:int` | Nombre de fichiers traités avec succès. |
| `*`fileErrorCount`*` | `xsd:int` | Nombre de fichiers à l’origine d’une erreur. |
| `*`fileWarningCount`*` | `xsd:int` | Nombre de fichiers qui ont généré un avertissement. |
| `*`fileDuplicateCount`*` | `xsd:int` | Nombre de fichiers de duplicata. |
| `*`fileUpdateCount`*` | `xsd:int` | Nombre de fichiers mis à jour. |
| `*`totalFileCount`*` | `xsd:int` | Nombre de fichiers traités par la tâche enregistrée. |
| `*`transferSuccessCount`*` | `xsd:int` | Nombre de transferts réussis. |
| `*`transferErrorCount`*` | `xsd:int` | Nombre d&#39;erreurs de transfert. |
| `*`transferWarningCount`*` | `xsd:int` | Nombre d&#39;avertissements de transfert. |
| `*`fatalError`*` | `xsd:boolean` | Indique si la tâche a généré une erreur irrécupérable. |
| `*`detailTotalRows`*` | `xsd:int` | Nombre total de lignes correspondant à la requête, qui peut être supérieur à la taille de `detailArray` en raison des limites de taille de page. |
| `*`detailArray`*` | `types:JobLogDetailArray` | Tableau des détails sur la tâche enregistrée. |

