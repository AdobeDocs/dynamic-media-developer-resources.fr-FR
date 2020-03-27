---
description: Journal des tâches une fois la tâche exécutée.
seo-description: Journal des tâches une fois la tâche exécutée.
seo-title: JobLog
solution: Experience Manager
title: JobLog
topic: Scene7 Image Production System API
uuid: d267009a-e4ad-4a21-ae0e-caf51d2f338b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JobLog{#joblog}

Journal des tâches une fois la tâche exécutée.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` |  poignée. |
| ` *`jobHandle`*` | `xsd:string` | Poignée de tâche. |
| ` *`jobName`*` | `xsd:string` | Nom de la tâche. |
| ` *`originalJobName`*` | `xsd:string` | Nom d’origine envoyé pour la tâche avec `submitJob`. |
| ` *`submitUserEmail`*` | `xsd:string` | Adresse électronique de l’utilisateur qui a envoyé la tâche. |
| ` *`logType`*` | `xsd:string` | Choix des types de journaux des tâches. |
| ` *`jobSubType`*` | `xsd:string` | Informations supplémentaires sur la tâche. |
| ` *`startDate`*` | `xsd:dateTime` | Le  la date, l’heure et le fuseau horaire de la tâche. |
| ` *`endDate`*` | `xsd:dateTime` | Date, heure et fuseau horaire de fin de la tâche. |
| ` *`description`*` | `xsd:string` | Description de la tâche telle qu’elle a été initialement spécifiée dans `submitJob`. |
| ` *`fileSuccessCount`*` | `xsd:int` | Nombre de fichiers traités avec succès. |
| ` *`fileErrorCount`*` | `xsd:int` | Nombre de fichiers à l’origine d’une erreur. |
| ` *`fileWarningCount`*` | `xsd:int` | Nombre de fichiers qui ont généré un avertissement. |
| ` *`fileDuplicateCount`*` | `xsd:int` | Nombre de fichiers . |
| ` *`fileUpdateCount`*` | `xsd:int` | Nombre de fichiers mis à jour. |
| ` *`totalFileCount`*` | `xsd:int` | Nombre de fichiers traités par la tâche enregistrée. |
| ` *`transferSuccessCount`*` | `xsd:int` | Nombre de transferts réussis. |
| ` *`transferErrorCount`*` | `xsd:int` | Nombre d&#39;erreurs de transfert. |
| ` *`transferWarningCount`*` | `xsd:int` | Nombre d’avertissements de transfert. |
| ` *`fatalError`*` | `xsd:boolean` | Indique si la tâche a généré une erreur irrécupérable. |
| ` *`detailTotalRows`*` | `xsd:int` | Nombre total de lignes correspondant au  du, qui peut être supérieur à la taille de `detailArray` en raison des limites de taille de page. |
| ` *`detailArray`*` | `types:JobLogDetailArray` | Tableau des détails sur la tâche enregistrée. |

