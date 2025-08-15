---
title: Résumé des ressources
description: Résultats de recherche de métadonnées contenant des informations résumées sur une ressource.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 10%

---

# [!DNL AssetSummary]{#assetsummary}

Résultats de recherche de métadonnées contenant des informations résumées sur une ressource.

Syntaxe

## Paramètres {#section-ebc75cc024d94c439260d2e71873cc74}

| Nom | Type | Description |
|---|---|---|
| assetHandle | `xsd:string` | Identifiant de ressource. |
| type | `xsd:string` | Type de ressource. La constante « Types de ressources » définit les valeurs possibles. Facultatif. |
| nom | `xsd:string` | Nom de la ressource. Facultatif. |
| dossier | `xsd:string` | Le dossier contenant la ressource. |
| filename | `xsd:string` | Nom de fichier de la ressource. |
| créé | `xsd:dateTime` | Date de création de la ressource. |
| createUser | `xsd:string` | L’utilisateur qui a créé la ressource. |
| lastModified | `xsd:dateTime` | Date de la dernière mise à jour de la ressource. |
| lastModifyUser | `xsd:string` | Dernier utilisateur à avoir modifié la ressource. |
| metadataArray | `types:MetadataArray` | Tableau de valeurs de métadonnées associées à la ressource. |
| score | `xsd:double` | Définit la précision en cas de recherche par analogie (0 = aucune correspondance, 1 = correspondance exacte). |
| scoreDetail | `xsd:string` | Il contient des informations détaillées sur des zones similaires à la suite d’une recherche par analogie. |
