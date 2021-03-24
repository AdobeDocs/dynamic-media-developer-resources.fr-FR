---
description: Renomme un projet.
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic, SDK/API, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 21%

---


# renameProject{#renameproject}

Renomme un projet.

Syntaxe

## Types d’utilisateur autorisés {#section-093d1f611a1647568e885ddd842b8f78}

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
| `*`companyName`*` | `xsd:string` | Oui | Gérer la société avec le projet que vous souhaitez renommer. |
| `*`projectHandle`*` | `xsd:string` | Oui | Traitement du projet. |
| `*`projectName`*` | `xsd:string` | Oui | Nouveau nom de projet. |

**Output (renameProjectParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Oui | Handle du projet renommé. |

## Exemples {#section-a0a06d9244774795b695a10b92b2a5e7}

Cet exemple de code renomme un projet et renvoie le nom d&#39;utilisateur du projet.

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

