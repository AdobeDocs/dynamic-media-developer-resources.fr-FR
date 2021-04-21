---
description: Crée un nouveau projet.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
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

