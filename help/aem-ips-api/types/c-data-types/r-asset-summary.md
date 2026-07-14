---
title: Résumé des ressources
description: Résultats de recherche de métadonnées contenant des informations résumées sur une ressource.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
TQID: 'https://experienceleague.adobe.com/RHT8NJiS0pGKUcrYGBsSI1vewvRGUCZmsPYP6Pb0OBs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 125
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

