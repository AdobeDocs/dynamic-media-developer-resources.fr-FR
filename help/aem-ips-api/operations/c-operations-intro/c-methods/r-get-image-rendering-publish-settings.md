---
description: Pour un usage interne uniquement. Voir la section Attributs de catalogue de références de catalogue de matériaux de rendu d’images.
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 16%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Pour un usage interne uniquement. Voir la section Attributs de catalogue de références de catalogue de matériaux de rendu d’images.

Syntaxe

## Types d’utilisateur autorisés {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-4f2cb8c589384816bb2525654ec49963}

**Entrée (getImageRenderingPublishSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Identifiant de la société dont vous souhaitez obtenir les paramètres de publication de rendu d’image. |
| `*`contextHandle`*` | `xsd:string` | Oui | Traitement du contexte de publication. |

**Output (getImageRenderingPublishSettingsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | Oui | Paramètres de publication de rendu d’image. |

