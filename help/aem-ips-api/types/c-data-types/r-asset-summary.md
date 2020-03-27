---
description: Résultats de la recherche de métadonnées contenant des informations résumées sur un fichier.
seo-description: Résultats de la recherche de métadonnées contenant des informations résumées sur un fichier.
seo-title: AssetSummary
solution: Experience Manager
title: AssetSummary
topic: Scene7 Image Production System API
uuid: 0ac8f900-c16c-409d-b83c-3bdf0ad28fac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetSummary{#assetsummary}

Résultats de la recherche de métadonnées contenant des informations résumées sur un fichier.

Syntaxe

## Paramètres {#section-ebc75cc024d94c439260d2e71873cc74}

| Nom | Type | Description |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Poignée de ressource. |
| ` *`type`*` | `xsd:string` | Type de fichier. La constante &quot;Types de fichier&quot; définit les valeurs possibles. Facultatif. |
| ` *`nom`*` | `xsd:string` | Nom du fichier. Facultatif. |
| ` *`dossier`*` | `xsd:string` | Dossier contenant le fichier. |
| ` *`filename`*` | `xsd:string` | Nom de fichier du fichier. |
| ` *`créé`*` | `xsd:dateTime` | Date de création des ressources. |
| ` *`createUser`*` | `xsd:string` | Utilisateur qui a créé la ressource. |
| ` *`lastModified`*` | `xsd:dateTime` | Date de la dernière mise à jour de la ressource. |
| ` *`lastModifyUser`*` | `xsd:string` | Dernier utilisateur qui a modifié la ressource. |
| ` *`metadataArray`*` | `types:MetadataArray` | Tableau des valeurs de métadonnées associées au fichier. |
| ` *`score`*` | `xsd:double` | Définit la précision en cas de recherche par analogie (0 = aucune correspondance, 1 = correspondance exacte). |
| ` *`scoreDetail`*` | `xsd:string` | Contient des informations détaillées sur des zones similaires suite à une recherche par analogie. |

