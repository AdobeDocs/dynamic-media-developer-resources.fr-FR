---
description: Renomme un projet.
seo-description: Renomme un projet.
seo-title: renameProject
solution: Experience Manager
title: renameProject
topic: Scene7 Image Production System API
uuid: 6303c493-a6fe-4b32-80c3-947aba4190f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# renameProject{#renameproject}

Renomme un projet.

Syntaxe

## Types d’utilisateurs autorisés {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-43ccd77648784be4a259a723c3e1db40}

**Input (renameProjectParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Oui | Gérez vers le le projet que vous souhaitez renommer. |
| ` *`projectHandle`*` | `xsd:string` | Oui | Gestion du projet. |
| ` *`projectName`*` | `xsd:string` | Oui | Nouveau nom du projet. |

**Output (renameProjectParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`projectHandle`*` | `xsd:string` | Oui | Gestionnaire du projet renommé. |

## Exemples {#section-a0a06d9244774795b695a10b92b2a5e7}

Cet exemple de code renomme un projet et renvoie le nom d’utilisateur du projet.

**Request**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**Réponse**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```

