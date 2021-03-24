---
description: Met à jour les paramètres de configuration de la visionneuse SWF.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic, SDK/API, paramètres prédéfinis de la visionneuse
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
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
