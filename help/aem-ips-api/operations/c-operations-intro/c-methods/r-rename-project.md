---
description: Renomme un projet.
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 23%

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

**Entrée (renameProjectParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyName | `xsd:string` | Oui | Gérer l’entreprise avec le projet que vous souhaitez renommer. |
| projectHandle | `xsd:string` | Oui | Gérer au projet. |
| projectName | `xsd:string` | Oui | Nouveau nom du projet. |

**Sortie (renameProjectParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| projectHandle | `xsd:string` | Oui | Gestionnaire du projet renommé. |

## Exemples {#section-a0a06d9244774795b695a10b92b2a5e7}

Cet exemple de code renomme un projet et renvoie la gestion du projet.

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
