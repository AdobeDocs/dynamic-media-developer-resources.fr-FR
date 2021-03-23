---
description: Supprime un format de publication de vignette.
seo-description: Supprime un format de publication de vignette.
seo-title: deleteVignettePublishFormat
solution: Experience Manager
title: deleteVignettePublishFormat
uuid: 3c8148d5-dec6-4ffa-8ab8-2cd70811ada6
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

---


# deleteVignettePublishFormat{#deletevignettepublishformat}

Supprime un format de publication de vignette.

## Types d’utilisateur autorisés {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-789625ba29df4b5f880914d4c64f77ce}

**Entrée (deleteVignettePublishFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société à laquelle appartient la vignette. |
| `*`vignetteFormatHandle`*` | `xsd:string` | Oui | Poignée du format de publication de la vignette à supprimer. |

**Output (deleteVignettePublishFormatParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Cet exemple de code supprime un format de publication de vignette spécifié par son handle.

**Request**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Réponse**

Aucune
