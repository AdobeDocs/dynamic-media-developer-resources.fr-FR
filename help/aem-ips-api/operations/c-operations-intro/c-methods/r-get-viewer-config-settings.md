---
description: Obtient tous les paramètres de configuration de la visionneuse associés à la ressource spécifiée.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 22%

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
| CompanyHandle | `xsd:string` | Oui | Manipuler à la société. |
| AssetHandle | `xsd:string` | Oui | Poignée pour la ressource. |

**Output (getViewerCoinfigSettingsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| type | `xsd:string` | Oui | Type de visionneuse auquel s’appliquent les paramètres de configuration. |
| Paramètre configSettingsArray | `types:ConfigSettingsArray` | Oui | Tableau des paramètres de configuration de la visionneuse. |
