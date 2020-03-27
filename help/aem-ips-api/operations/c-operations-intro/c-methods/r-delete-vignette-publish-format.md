---
description: Supprime un format de publication de vignette.
seo-description: Supprime un format de publication de vignette.
seo-title: deleteVideoPublishFormat
solution: Experience Manager
title: deleteVideoPublishFormat
topic: Scene7 Image Production System API
uuid: 3c8148d5-dec6-4ffa-8ab8-2cd70811ada6
translation-type: tm+mt
source-git-commit: d3766bba78cd1051538ff6a94f61ba61e989f1a5

---


# deleteVideoPublishFormat{#deletevignettepublishformat}

Supprime un format de publication de vignette.

## Types d’utilisateurs autorisés {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-789625ba29df4b5f880914d4c64f77ce}

**Entrée (deleteVignettePublishFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée du auquel appartient la vignette. |
| ` *`vignetteFormatHandle`*` | `xsd:string` | Oui | Poignée du format de publication de vignette à supprimer. |

**Output (deleteVignettePublishFormatParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Cet exemple de code supprime un format de publication de vignette spécifié par son gestionnaire.

**Request**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Réponse**

Aucune
