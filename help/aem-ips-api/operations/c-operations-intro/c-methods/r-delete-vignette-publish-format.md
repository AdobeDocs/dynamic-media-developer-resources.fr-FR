---
description: Supprime un format de publication de vignette.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
TQID: 'https://experienceleague.adobe.com/e1qIrpGHPuodTx79J1ke-7ULFptiCa6ZoIXyldJvSBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 12%

---

# deleteVignettePublishFormat{#deletevignettepublishformat}

Supprime un format de publication de vignette.

## Types d’utilisateurs autorisés {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-789625ba29df4b5f880914d4c64f77ce}

**Input (deleteVignettePublishFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Poignée de la société à laquelle appartient la vignette. |
| vignetteFormatHandle | `xsd:string` | Oui | Identifiant du format de publication de la vignette à supprimer. |

**Output (deleteVignettePublishFormatParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Cet exemple de code supprime un format de publication de vignette spécifié par son descripteur.

**Requête**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Réponse**

Aucune

