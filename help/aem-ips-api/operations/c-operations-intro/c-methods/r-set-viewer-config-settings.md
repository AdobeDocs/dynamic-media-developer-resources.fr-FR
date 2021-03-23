---
description: Associe les paramètres de configuration de la visionneuse à un fichier. Il peut s’agir d’un paramètre prédéfini de visionneuse ou du fichier source de la visionneuse.
seo-description: Associe les paramètres de configuration de la visionneuse à un fichier. Il peut s’agir d’un paramètre prédéfini de visionneuse ou du fichier source de la visionneuse.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
uuid: d83d866e-9243-479f-9b33-727aad8158e5
feature: Dynamic Media Classic, SDK/API, paramètres prédéfinis de la visionneuse
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---


# setViewerConfigSettings{#setviewerconfigsettings}

Associe les paramètres de configuration de la visionneuse à un fichier. Il peut s’agir d’un paramètre prédéfini de visionneuse ou du fichier source de la visionneuse.

Syntaxe

## Types d’utilisateur autorisés {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-bcc8c83cc84141e8b1341be9133e8511}

**Entrée (setViewerConfigSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Pose la société. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de ressource. |
| `*`name`*` | `xsd:string` | Oui | Nom du fichier. |
| `*`type`*` | `xsd:string` | Oui | Type de fichier auquel vous souhaitez appliquer la configuration de la visionneuse. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Oui | Tableau de `ConfigSettings` appliqué à la ressource. |

**Output (setViewerConfigSettingsParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.
