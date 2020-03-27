---
description: Obtient tous les paramètres de configuration de la visionneuse associés à la ressource spécifiée.
seo-description: Obtient tous les paramètres de configuration de la visionneuse associés à la ressource spécifiée.
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
topic: Scene7 Image Production System API
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getViewerConfigSettings{#getviewerconfigsettings}

Obtient tous les paramètres de configuration de la visionneuse associés à la ressource spécifiée.

Syntaxe

## Types d’utilisateurs autorisés {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-7d06abf3d707494c8a1270c7fa1477f1}

**Entrée (getViewerConfigSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Pose le . |
| ` *`assetHandle`*` | `xsd:string` | Oui | Traitement de la ressource. |

**Output (getViewerConfigSettingsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`type`*` | `xsd:string` | Oui | Type de lecteur auquel s’appliquent les paramètres de configuration. |
| ` *`configSettingsArray`*` | `types:ConfigSettingsArray` | Oui | Tableau des paramètres de configuration de la visionneuse. |

