---
description: Pour usage interne uniquement. Reportez-vous à la section Attributs de catalogue de référence de rendus d'images.
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
TQID: 'https://experienceleague.adobe.com/-zBv9N9COcH6KjyHfgjYF4TXblntNiZMVBB6nr-oe2w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 17%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Pour usage interne uniquement. Reportez-vous à la section Attributs de catalogue de référence de rendus d&#39;images.

Syntaxe

## Types d’utilisateurs autorisés {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-4f2cb8c589384816bb2525654ec49963}

**Input (getImageRenderingPublishSettingsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société dont vous souhaitez obtenir les paramètres de publication de rendu d’image. |
| contextHandle | `xsd:string` | Oui | Gérer vers le contexte de publication. |

**Output (getImageRenderingPublishSettingsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| publishSettingsArray | `type:ConfigSettingArray` | Oui | Paramètres de publication du rendu des images. |

