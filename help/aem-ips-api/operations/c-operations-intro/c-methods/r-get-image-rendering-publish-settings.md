---
description: Pour une utilisation interne uniquement. Voir la section Attributs de catalogue de matières de rendu d’images .
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 16%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Pour une utilisation interne uniquement. Voir la section Attributs de catalogue de matières de rendu d’images .

Syntaxe

## Types d’utilisateurs autorisés {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-4f2cb8c589384816bb2525654ec49963}

**Entrée (getImageRenderingPublishSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gestionnaire de l’entreprise dont vous souhaitez obtenir les paramètres de publication de rendu d’image. |
| `*`contextHandle`*` | `xsd:string` | Oui | Gérer au contexte de publication. |

**Sortie (getImageRenderingPublishSettingsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | Oui | Paramètres de publication du rendu des images. |
