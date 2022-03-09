---
description: Journal des tâches une fois la tâche exécutée.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 4%

---

# JobLog{#joblog}

Journal des tâches une fois la tâche exécutée.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| companyHandle | `xsd:string` | Poignée de la société. |
| jobHandle | `xsd:string` | Poignée de tâche. |
| jobName | `xsd:string` | Nom de la tâche. |
| originalJobName | `xsd:string` | Nom original envoyé pour la tâche avec `submitJob`. |
| submitUserEmail | `xsd:string` | Adresse électronique de l’utilisateur qui a envoyé la tâche. |
| logType | `xsd:string` | Choix des types de logs de traitement. |
| jobSubType | `xsd:string` | Informations supplémentaires sur la tâche. |
| startDate | `xsd:dateTime` | Date, heure et fuseau horaire de début de la tâche. |
| endDate | `xsd:dateTime` | Date, heure et fuseau horaire de fin de la tâche. |
| description | `xsd:string` | Description de la tâche telle qu’elle est spécifiée à l’origine dans `submitJob`. |
| fileSuccessCount | `xsd:int` | Nombre de fichiers traités avec succès. |
| fileErrorCount | `xsd:int` | Nombre de fichiers à l’origine d’une erreur. |
| fileWarningCount | `xsd:int` | Nombre de fichiers ayant généré un avertissement. |
| fileDuplicateCount | `xsd:int` | Nombre de fichiers dupliqués. |
| fileUpdateCount | `xsd:int` | Nombre de fichiers mis à jour. |
| totalFileCount | `xsd:int` | Nombre de fichiers traités par la tâche enregistrée. |
| transferSuccessCount | `xsd:int` | Nombre de transferts réussis. |
| transferErrorCount | `xsd:int` | Nombre d&#39;erreurs de transfert. |
| transferWarningCount | `xsd:int` | Nombre d’avertissements de transfert. |
| fatalError | `xsd:boolean` | Si la tâche a généré une erreur fatale. |
| detailTotalRows | `xsd:int` | Le nombre total de lignes correspondant à la requête, qui peut être supérieur à la taille de `detailArray` en raison des limites de taille de page. |
| detailArray | `types:JobLogDetailArray` | Tableau de détails sur la tâche consignée. |
