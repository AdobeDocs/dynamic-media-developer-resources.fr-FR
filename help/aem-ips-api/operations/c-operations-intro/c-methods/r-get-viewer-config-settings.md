---
description: Obtient tous les paramètres de configuration de la visionneuse associés à la ressource spécifiée.
seo-description: Obtient tous les paramètres de configuration de la visionneuse associés à la ressource spécifiée.
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
feature: Dynamic Media Classic, SDK/API, paramètres prédéfinis de la visionneuse
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 17%

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

