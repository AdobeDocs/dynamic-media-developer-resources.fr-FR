---
description: Met à jour les paramètres de configuration de la visionneuse de SWF.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 15%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

Met à jour les paramètres de configuration de la visionneuse de SWF.

Syntaxe

## Types d’utilisateurs autorisés {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-29790d933fb24aa392d0cb2d52d1310f}

**Entrée (updateViewerConfigSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Traitez la société. |
| assetHandle | `xsd:string` | Oui | Poignée de ressource. |
| configSettingArray | `types:ConfigSettingArray` | Oui | Tableau des paramètres de configuration à appliquer à la visionneuse. |

**Sortie (updateViewerConfigSettingsReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.
