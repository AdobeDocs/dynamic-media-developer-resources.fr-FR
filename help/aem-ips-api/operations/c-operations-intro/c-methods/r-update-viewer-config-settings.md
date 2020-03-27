---
description: Met à jour les paramètres de configuration du lecteur SWF.
seo-description: Met à jour les paramètres de configuration du lecteur SWF.
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
topic: Scene7 Image Production System API
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateViewerConfigSettings{#updateviewerconfigsettings}

Met à jour les paramètres de configuration du lecteur SWF.

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
| ` *`companyHandle`*` | `xsd:string` | Oui | Pose le . |
| ` *`assetHandle`*` | `xsd:string` | Oui | Poignée de ressource. |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | Oui | Tableau des paramètres de configuration que vous souhaitez appliquer au lecteur de contenu. |

**Output (updateViewerConfigSettingsReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.
