---
description: Associe les paramètres de configuration de la visionneuse à une ressource. Il peut s’agir d’un paramètre prédéfini de visionneuse ou de la ressource source de la visionneuse.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Paramètres prédéfinis de la visionneuse
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 11%

---

# setViewerConfigSettings{#setviewerconfigsettings}

Associe les paramètres de configuration de la visionneuse à une ressource. Il peut s’agir d’un paramètre prédéfini de visionneuse ou de la ressource source de la visionneuse.

Syntaxe

## Types d’utilisateurs autorisés {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-bcc8c83cc84141e8b1341be9133e8511}

**Entrée (setViewerConfigSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gérer la société. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de ressource. |
| `*`name`*` | `xsd:string` | Oui | Nom de la ressource. |
| `*`type`*` | `xsd:string` | Oui | Type de ressource auquel vous souhaitez appliquer la configuration de la visionneuse. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Oui | Tableau de `ConfigSettings` appliqué à la ressource. |

**Sortie (setViewerConfigSettingsParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.
