---
description: Obtient tous les paramètres de configuration de la visionneuse associés à la ressource spécifiée.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Paramètres prédéfinis de la visionneuse
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

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
| `*`companyHandle`*` | `xsd:string` | Oui | Gérer la société. |
| `*`assetHandle`*` | `xsd:string` | Oui | Gérer la ressource. |

**Sortie (getViewerConfigSettingsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`type`*` | `xsd:string` | Oui | Type de visionneuse auquel s’appliquent les paramètres de configuration. |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | Oui | Tableau des paramètres de configuration de la visionneuse. |
