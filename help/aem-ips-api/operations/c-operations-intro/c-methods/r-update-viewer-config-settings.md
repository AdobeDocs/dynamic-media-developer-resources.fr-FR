---
description: Met à jour les paramètres de configuration de la visionneuse SWF.
seo-description: Met à jour les paramètres de configuration de la visionneuse SWF.
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 13%

---


# updateViewerConfigSettings{#updateviewerconfigsettings}

Met à jour les paramètres de configuration de la visionneuse SWF.

Syntaxe

## Types d’utilisateur autorisés {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-29790d933fb24aa392d0cb2d52d1310f}

**Entrée (updateViewerConfigSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Pose la société. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de ressource. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Oui | Tableau des paramètres de configuration à appliquer au lecteur. |

**Sortie (updateViewerConfigSettingsReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.
