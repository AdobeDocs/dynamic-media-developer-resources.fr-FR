---
description: Obtient tous les paramètres de configuration de la visionneuse associés à la ressource spécifiée.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 19%

---


# getViewerConfigSettings{#getviewerconfigsettings}

Obtient tous les paramètres de configuration de la visionneuse associés à la ressource spécifiée.

Syntaxe

## Types d’utilisateur autorisés {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-7d06abf3d707494c8a1270c7fa1477f1}

**Entrée (getViewerConfigSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Pose la société. |
| `*`assetHandle`*` | `xsd:string` | Oui | Traitez le fichier. |

**Output (getViewerConfigSettingsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`type`*` | `xsd:string` | Oui | Type de lecteur auquel s’appliquent les paramètres de configuration. |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | Oui | Tableau des paramètres de configuration de la visionneuse. |

