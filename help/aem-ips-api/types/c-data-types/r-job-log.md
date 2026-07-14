---
description: Le log de traitement une fois le traitement exécuté.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
TQID: 'https://experienceleague.adobe.com/R3h5NRNxH00Qskdzvw6ul55STF234SudJbjLGYrd238'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 187
ht-degree: 2%

---

# [!DNL JobLog]{#joblog}

Le log de traitement une fois le traitement exécuté.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| companyHandle | `xsd:string` | Identifiant de la société. |
| jobHandle | `xsd:string` | Traitement du traitement. |
| jobName | `xsd:string` | Nom du traitement. |
| originalJobName | `xsd:string` | Nom d’origine envoyé pour la tâche avec `submitJob`. |
| submitUserEmail | `xsd:string` | Adresse e-mail de l’utilisateur qui a envoyé le traitement. |
| logType | `xsd:string` | Choix des types de logs de traitement. |
| jobSubType | `xsd:string` | Informations supplémentaires sur le travail. |
| startDate | `xsd:dateTime` | Date, heure et fuseau horaire de début de la tâche. |
| endDate | `xsd:dateTime` | Date, heure et fuseau horaire de fin de la tâche. |
| [!DNL description] | `xsd:string` | Description du traitement telle qu’initialement spécifiée dans `submitJob`. |
| fileSuccessCount | `xsd:int` | Nombre de fichiers traités avec succès |
| fileErrorCount | `xsd:int` | Nombre de fichiers ayant provoqué une erreur. |
| fileWarningCount | `xsd:int` | Nombre de fichiers ayant généré un avertissement. |
| fileDuplicateCount | `xsd:int` | Nombre de fichiers en double. |
| fileUpdateCount | `xsd:int` | Nombre de fichiers mis à jour. |
| totalFileCount | `xsd:int` | Nombre de fichiers traités par la tâche consignée. |
| transferSuccessCount | `xsd:int` | Nombre de transferts réussis. |
| transferErrorCount | `xsd:int` | Nombre d’erreurs de transfert. |
| transferWarningCount | `xsd:int` | Nombre d’avertissements de transfert. |
| fatalError | `xsd:boolean` | Indique si le traitement a généré une erreur irrécupérable. |
| detailTotalRows | `xsd:int` | Nombre total de lignes correspondant à la requête, qui peut être supérieur à la taille de `detailArray` en raison des limites de taille de page. |
| detailArray | `types:JobLogDetailArray` | Tableau de détails sur la tâche consignée. |

