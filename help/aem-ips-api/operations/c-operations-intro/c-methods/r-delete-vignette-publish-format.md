---
description: Supprime le format de publication d’une vignette.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 13%

---

# deleteVignettePublishFormat{#deletevignettepublishformat}

Supprime le format de publication d’une vignette.

## Types d’utilisateurs autorisés {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-789625ba29df4b5f880914d4c64f77ce}

**Entrée (deleteVignettePublishFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée à la société à laquelle appartient la vignette. |
| `*`vignetteFormatHandle`*` | `xsd:string` | Oui | Gestion du format de publication de la vignette à supprimer. |

**Sortie (deleteVignettePublishFormatParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Cet exemple de code supprime le format de publication d’une vignette spécifié par sa poignée.

**Request**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Réponse**

Aucune
