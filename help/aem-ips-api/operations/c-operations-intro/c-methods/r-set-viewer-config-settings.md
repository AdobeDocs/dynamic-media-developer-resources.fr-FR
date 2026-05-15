---
description: Associe les paramètres de configuration de la visionneuse à une ressource. Il peut s’agir d’un paramètre prédéfini de visionneuse ou de la ressource source de la visionneuse.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
TQID: 'https://experienceleague.adobe.com/MX6dj-7j6HfNSISaWFheorOZYVnszSY24OuuUGdKvPA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 12%

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

**Input (setViewerConfigSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gérer vers la société. |
| assetHandle | `xsd:string` | Oui | Identifiant de ressource. |
| nom | `xsd:string` | Oui | Nom de la ressource. |
| type | `xsd:string` | Oui | Type de ressource auquel vous souhaitez appliquer la configuration de visionneuse. |
| configSettingArray | `types:ConfigSettingArray` | Oui | Tableau des `ConfigSettings` appliqués à la ressource. |

**Output (setViewerConfigSettingsParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.
