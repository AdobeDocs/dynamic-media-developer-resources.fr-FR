---
description: Crée un projet.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 18%

---

# createProject{#createproject}

Crée un projet.

Syntaxe

## Types d’utilisateurs autorisés {#section-17878e2e4c3a44988c9a1af82c2ac319}

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
| companyHandle | `xsd:string` | Oui | Identifiant de la société associée au nouveau projet. |
| projectName | `xsd:string` | Oui | Nouveau nom du projet. |

**Output (createProjectParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| projectHandle | `xsd:string` | Oui | La poignée du nouveau projet. |

## Exemples {#section-a0cd532b67e346d088fbec141231a0e5}

Cet exemple de code crée un projet appelé `ApiTestProject` dans une société spécifiée par son descripteur. La réponse renvoie la poignée au projet.

**Requête**

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
