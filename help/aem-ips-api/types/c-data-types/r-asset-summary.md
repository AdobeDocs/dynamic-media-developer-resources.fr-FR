---
description: Résultats de la recherche de métadonnées contenant des informations résumées sur une ressource.
solution: Experience Manager
title: AssetSummary
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# [!DNL AssetSummary]{#assetsummary}

Résultats de la recherche de métadonnées contenant des informations résumées sur une ressource.

Syntaxe

## Paramètres {#section-ebc75cc024d94c439260d2e71873cc74}

| Nom | Type | Description |
|---|---|---|
| assetHandle | `xsd:string` | Poignée de ressource. |
| type | `xsd:string` | Type de fichier. La constante &quot;Types de ressources&quot; définit les valeurs possibles. Facultatif. |
| name | `xsd:string` | Nom de la ressource. Facultatif. |
| dossier | `xsd:string` | Dossier contenant la ressource. |
| filename | `xsd:string` | Nom de fichier de la ressource. |
| créé | `xsd:dateTime` | Date de création de la ressource. |
| createUser | `xsd:string` | L’utilisateur qui a créé la ressource. |
| lastModified | `xsd:dateTime` | Date de la dernière mise à jour de la ressource. |
| lastModifyUser | `xsd:string` | Dernier utilisateur à avoir modifié la ressource. |
| metadataArray | `types:MetadataArray` | Tableau des valeurs de métadonnées associées à la ressource. |
| score | `xsd:double` | Définit la précision en cas de recherche par analogie (0 = aucune correspondance, 1 = correspondance exacte). |
| scoreDetail | `xsd:string` | Contient des informations détaillées sur des zones similaires suite à une recherche par analogie. |
