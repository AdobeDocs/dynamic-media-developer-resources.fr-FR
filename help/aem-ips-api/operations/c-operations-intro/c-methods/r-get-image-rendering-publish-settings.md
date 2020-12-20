---
description: Pour un usage interne uniquement. Voir la section Attributs de catalogue de références de catalogue de matériaux de rendu d’images.
seo-description: Pour un usage interne uniquement. Voir la section Attributs de catalogue de références de catalogue de matériaux de rendu d’images.
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
topic: Scene7 Image Production System API
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 14%

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
| ` *`companyHandle`*` | `xsd:string` | Oui | Identifiant de la société dont vous souhaitez obtenir les paramètres de publication de rendu d’image. |
| ` *`contextHandle`*` | `xsd:string` | Oui | Traitement du contexte de publication. |

**Output (getImageRenderingPublishSettingsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`publishSettingsArray`*` | `type:ConfigSettingArray` | Oui | Paramètres de publication de rendu d’image. |

