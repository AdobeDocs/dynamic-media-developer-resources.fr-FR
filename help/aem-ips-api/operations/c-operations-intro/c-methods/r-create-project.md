---
description: Crée un nouveau projet.
seo-description: Crée un nouveau projet.
seo-title: createProject
solution: Experience Manager
title: createProject
topic: Dynamic Media Image Production System API
uuid: e011b7ba-6c15-47ef-9ea1-6189c37e7719
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 18%

---


# createProject{#createproject}

Crée un nouveau projet.

Syntaxe

## Types d’utilisateur autorisés {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-8c741884eb54489bbaad0c444fee80b6}

**Entrée (createProjectParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société associée au nouveau projet. |
| `*`projectName`*` | `xsd:string` | Oui | Nouveau nom de projet. |

**Output (createProjectParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Oui | Poignée du nouveau projet. |

## Exemples {#section-a0cd532b67e346d088fbec141231a0e5}

Cet exemple de code crée un projet appelé `ApiTestProject` dans une société spécifiée par son handle. La réponse renvoie la poignée au projet.

**Request**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```

